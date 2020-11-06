---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536075"
---
# <span data-ttu-id="12ae4-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="12ae4-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="12ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="12ae4-103">구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ae4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12ae4-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ae4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="12ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="12ae4-106">**AzureRmImageConfig** cmdlet은 구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="12ae4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="12ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="12ae4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="12ae4-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="12ae4-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="12ae4-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="12ae4-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="12ae4-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="12ae4-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="12ae4-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="12ae4-115">변수</span><span class="sxs-lookup"><span data-stu-id="12ae4-115">PARAMETERS</span></span>

### <span data-ttu-id="12ae4-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="12ae4-116">-DataDisk</span></span>
<span data-ttu-id="12ae4-117">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-118">-위치</span><span class="sxs-lookup"><span data-stu-id="12ae4-118">-Location</span></span>
<span data-ttu-id="12ae4-119">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-119">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="12ae4-120">-OsDisk</span></span>
<span data-ttu-id="12ae4-121">운영 체제 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-121">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-122">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="12ae4-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="12ae4-123">원본 가상 컴퓨터 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-123">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-124">태그</span><span class="sxs-lookup"><span data-stu-id="12ae4-124">-Tag</span></span>
<span data-ttu-id="12ae4-125">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-126">-확인</span><span class="sxs-lookup"><span data-stu-id="12ae4-126">-Confirm</span></span>
<span data-ttu-id="12ae4-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ae4-128">-WhatIf</span></span>
<span data-ttu-id="12ae4-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12ae4-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ae4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ae4-131">CommonParameters</span></span>
<span data-ttu-id="12ae4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ae4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ae4-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ae4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ae4-134">입력</span><span class="sxs-lookup"><span data-stu-id="12ae4-134">INPUTS</span></span>

### <span data-ttu-id="12ae4-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="12ae4-135">System.String</span></span>
<span data-ttu-id="12ae4-136">System.webserver. ImageOSDisk. ImageDataDisk []을 (를) 대 한 모든. a.</span><span class="sxs-lookup"><span data-stu-id="12ae4-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="12ae4-137">출력</span><span class="sxs-lookup"><span data-stu-id="12ae4-137">OUTPUTS</span></span>

### <span data-ttu-id="12ae4-138">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="12ae4-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="12ae4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="12ae4-139">NOTES</span></span>

## <span data-ttu-id="12ae4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12ae4-140">RELATED LINKS</span></span>

