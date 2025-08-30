# Changelog

All notable changes to this project will be documented in this file.

## [2.0.0] - 2024-12-19

### 🚀 Major Modernization Update

This release brings the codebase up to date with the latest PyTorch and Python ecosystem, ensuring compatibility with modern development environments.

### ✨ Added
- Comprehensive `requirements.txt` with latest compatible versions
- Updated installation instructions in README.md
- CHANGELOG.md for tracking future updates

### 🔧 Changed
- **PyTorch Compatibility**: Updated to support PyTorch 2.0+ (tested with PyTorch 2.1+)
- **Python Compatibility**: Now supports Python 3.8+ (removed Python 2 compatibility code)
- **Dependencies**: Updated all major dependencies to their latest stable versions

### 🐛 Fixed
- **Critical**: Replaced deprecated `torch._utils._accumulate` with standard `itertools.accumulate`
- **Critical**: Removed `six` library dependency (Python 3 standard library now used)
- **Critical**: Updated `F.sigmoid` to `torch.sigmoid` (deprecated function)
- **Critical**: Fixed `grid_sample` compatibility issues for latest PyTorch
- **Critical**: Replaced `six.BytesIO` with `io.BytesIO`

### 📦 Dependencies Updated
- `torch>=2.0.0` (from 1.3.1)
- `torchvision>=0.15.0` (from legacy version)
- `numpy>=1.21.0` (from legacy version)
- `Pillow>=9.0.0` (from legacy version)
- `opencv-python>=4.5.0` (newly added)
- `lmdb>=1.4.0` (from legacy version)
- `natsort>=8.0.0` (from legacy version)
- `nltk>=3.8.0` (from legacy version)

### 🔄 Migration Notes
- **Breaking Change**: This version requires PyTorch 2.0+ and Python 3.8+
- **Installation**: Use `pip install -r requirements.txt` for easy setup
- **Backward Compatibility**: Legacy models and checkpoints remain compatible
- **Performance**: No performance regression, improved stability

### 🧪 Testing
- Tested with PyTorch 2.1.0, CUDA 11.8, Python 3.9
- Verified compatibility with existing pretrained models
- All core functionality (training, testing, demo) verified working

---

## [1.x.x] - Legacy Versions

For historical changes, please refer to the commit history and the original repository updates.

### Key Legacy Updates
- **Aug 3, 2020**: Added Baidu warpctc support
- **Dec 27, 2019**: Added FLOPS calculation and ICDAR2019-NormalizedED
- **Oct 22, 2019**: Added confidence score calculation
- **Jul 31, 2019**: Paper accepted at ICCV 2019
- **May 9, 2019**: Updated from PyTorch 1.0.1 to 1.1.0