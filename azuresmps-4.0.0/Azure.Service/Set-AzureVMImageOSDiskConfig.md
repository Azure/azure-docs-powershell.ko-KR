---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045444"
---
# <span data-ttu-id="ff824-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff824-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="ff824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff824-102">SYNOPSIS</span></span>
<span data-ttu-id="ff824-103">가상 컴퓨터 이미지의 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="ff824-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff824-104">SYNTAX</span></span>

### <span data-ttu-id="ff824-105">UpdateAzureVMImageParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff824-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ff824-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="ff824-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff824-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff824-107">DESCRIPTION</span></span>
<span data-ttu-id="ff824-108">**AzureVMImageOSDiskConfig** cmdlet은 가상 컴퓨터 이미지에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="ff824-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ff824-109">EXAMPLES</span></span>

### <span data-ttu-id="ff824-110">예제 1: 가상 컴퓨터 이미지에서 운영 체제 디스크 속성 설정</span><span class="sxs-lookup"><span data-stu-id="ff824-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="ff824-111">이 예제에서는 가상 컴퓨터 이미지에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="ff824-112">변수</span><span class="sxs-lookup"><span data-stu-id="ff824-112">PARAMETERS</span></span>

### <span data-ttu-id="ff824-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff824-113">-DiskConfig</span></span>
<span data-ttu-id="ff824-114">운영 체제 디스크 및 데이터 디스크 개체를 캡슐화 하는 디스크 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="ff824-115">-HostCaching</span></span>
<span data-ttu-id="ff824-116">운영 체제 디스크에 대 한 호스트 캐시 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="ff824-117">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-117">Valid values are:</span></span>

<span data-ttu-id="ff824-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ff824-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff824-119">-InformationAction</span></span>
<span data-ttu-id="ff824-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff824-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff824-122">하기로</span><span class="sxs-lookup"><span data-stu-id="ff824-122">Continue</span></span>
- <span data-ttu-id="ff824-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="ff824-123">Ignore</span></span>
- <span data-ttu-id="ff824-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="ff824-124">Inquire</span></span>
- <span data-ttu-id="ff824-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff824-125">SilentlyContinue</span></span>
- <span data-ttu-id="ff824-126">중지가</span><span class="sxs-lookup"><span data-stu-id="ff824-126">Stop</span></span>
- <span data-ttu-id="ff824-127">대기</span><span class="sxs-lookup"><span data-stu-id="ff824-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff824-128">-InformationVariable</span></span>
<span data-ttu-id="ff824-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="ff824-130">-MediaLink</span></span>
<span data-ttu-id="ff824-131">새 데이터 디스크가 추가 될 때 새 가상 하드 드라이브가 만들어지는 위치의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-132">-OS</span><span class="sxs-lookup"><span data-stu-id="ff824-132">-OS</span></span>
<span data-ttu-id="ff824-133">디스크 구성의 운영 체제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="ff824-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-134">Valid values are:</span></span>

- <span data-ttu-id="ff824-135">창을</span><span class="sxs-lookup"><span data-stu-id="ff824-135">Windows</span></span>
- <span data-ttu-id="ff824-136">Linux</span><span class="sxs-lookup"><span data-stu-id="ff824-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="ff824-137">-OSState</span></span>
<span data-ttu-id="ff824-138">가상 컴퓨터 이미지의 운영 체제 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="ff824-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-139">Valid values are:</span></span>

- <span data-ttu-id="ff824-140">Generalize</span><span class="sxs-lookup"><span data-stu-id="ff824-140">Generalized</span></span>
- <span data-ttu-id="ff824-141">위한</span><span class="sxs-lookup"><span data-stu-id="ff824-141">Specialized</span></span>

<span data-ttu-id="ff824-142">이 매개 변수를 사용 하면 가상 컴퓨터 이미지를 Azure로 캡처할 의도가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff824-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff824-143">CommonParameters</span></span>
<span data-ttu-id="ff824-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff824-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff824-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff824-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff824-146">입력</span><span class="sxs-lookup"><span data-stu-id="ff824-146">INPUTS</span></span>

## <span data-ttu-id="ff824-147">출력</span><span class="sxs-lookup"><span data-stu-id="ff824-147">OUTPUTS</span></span>

### <span data-ttu-id="ff824-148">WindowsAzure. ServiceManagement. m m/. m a m 설정</span><span class="sxs-lookup"><span data-stu-id="ff824-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="ff824-149">상속자</span><span class="sxs-lookup"><span data-stu-id="ff824-149">NOTES</span></span>

## <span data-ttu-id="ff824-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff824-150">RELATED LINKS</span></span>

[<span data-ttu-id="ff824-151">제거-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff824-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


