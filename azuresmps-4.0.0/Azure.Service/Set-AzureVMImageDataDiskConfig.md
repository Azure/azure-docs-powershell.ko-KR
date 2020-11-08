---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045436"
---
# <span data-ttu-id="4d949-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4d949-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="4d949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d949-102">SYNOPSIS</span></span>
<span data-ttu-id="4d949-103">가상 컴퓨터 이미지에 데이터 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="4d949-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d949-104">SYNTAX</span></span>

### <span data-ttu-id="4d949-105">UpdateAzureVMImageParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d949-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d949-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="4d949-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4d949-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d949-107">DESCRIPTION</span></span>
<span data-ttu-id="4d949-108">**AzureVMImageDataDiskConfig** cmdlet은 가상 컴퓨터 이미지의 데이터 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="4d949-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4d949-109">EXAMPLES</span></span>

### <span data-ttu-id="4d949-110">예제 1: 가상 컴퓨터 이미지에서 데이터 디스크 속성 설정</span><span class="sxs-lookup"><span data-stu-id="4d949-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="4d949-111">이 명령은 가상 컴퓨터에서 데이터 디스크 속성을 설정 하 고 가상 컴퓨터 이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="4d949-112">변수</span><span class="sxs-lookup"><span data-stu-id="4d949-112">PARAMETERS</span></span>

### <span data-ttu-id="4d949-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="4d949-113">-DataDiskName</span></span>
<span data-ttu-id="4d949-114">이 cmdlet이 구성 하는 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d949-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="4d949-115">-DiskConfig</span></span>
<span data-ttu-id="4d949-116">운영 체제 디스크 및 데이터 디스크 개체를 캡슐화 하는 디스크 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="4d949-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="4d949-117">-HostCaching</span></span>
<span data-ttu-id="4d949-118">운영 체제 디스크에 대 한 호스트 캐시 특성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="4d949-119">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-119">Valid values are:</span></span>

<span data-ttu-id="4d949-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d949-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d949-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4d949-121">-InformationAction</span></span>
<span data-ttu-id="4d949-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4d949-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d949-124">하기로</span><span class="sxs-lookup"><span data-stu-id="4d949-124">Continue</span></span>
- <span data-ttu-id="4d949-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="4d949-125">Ignore</span></span>
- <span data-ttu-id="4d949-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="4d949-126">Inquire</span></span>
- <span data-ttu-id="4d949-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4d949-127">SilentlyContinue</span></span>
- <span data-ttu-id="4d949-128">중지가</span><span class="sxs-lookup"><span data-stu-id="4d949-128">Stop</span></span>
- <span data-ttu-id="4d949-129">대기</span><span class="sxs-lookup"><span data-stu-id="4d949-129">Suspend</span></span>

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

### <span data-ttu-id="4d949-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4d949-130">-InformationVariable</span></span>
<span data-ttu-id="4d949-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4d949-132">-Lun</span><span class="sxs-lookup"><span data-stu-id="4d949-132">-Lun</span></span>
<span data-ttu-id="4d949-133">가상 컴퓨터에서 데이터 드라이브가 탑재 된 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d949-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="4d949-134">-MediaLink</span></span>
<span data-ttu-id="4d949-135">새 데이터 디스크가 추가 될 때 새 가상 하드 드라이브가 만들어지는 위치의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d949-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d949-136">CommonParameters</span></span>
<span data-ttu-id="4d949-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d949-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d949-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d949-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d949-139">입력</span><span class="sxs-lookup"><span data-stu-id="4d949-139">INPUTS</span></span>

## <span data-ttu-id="4d949-140">출력</span><span class="sxs-lookup"><span data-stu-id="4d949-140">OUTPUTS</span></span>

### <span data-ttu-id="4d949-141">WindowsAzure. ServiceManagement. m m/. m a m 설정</span><span class="sxs-lookup"><span data-stu-id="4d949-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="4d949-142">상속자</span><span class="sxs-lookup"><span data-stu-id="4d949-142">NOTES</span></span>

## <span data-ttu-id="4d949-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d949-143">RELATED LINKS</span></span>

[<span data-ttu-id="4d949-144">제거-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4d949-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


