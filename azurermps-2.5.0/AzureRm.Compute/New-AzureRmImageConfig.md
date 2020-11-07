---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880753"
---
# <span data-ttu-id="a864a-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="a864a-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="a864a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a864a-102">SYNOPSIS</span></span>
<span data-ttu-id="a864a-103">구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a864a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a864a-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a864a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a864a-105">DESCRIPTION</span></span>
<span data-ttu-id="a864a-106">**AzureRmImageConfig** cmdlet은 구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="a864a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a864a-107">EXAMPLES</span></span>

### <span data-ttu-id="a864a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a864a-108">Example 1</span></span>
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

<span data-ttu-id="a864a-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="a864a-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="a864a-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="a864a-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="a864a-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="a864a-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a864a-115">변수</span><span class="sxs-lookup"><span data-stu-id="a864a-115">PARAMETERS</span></span>

### <span data-ttu-id="a864a-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="a864a-116">-DataDisk</span></span>
<span data-ttu-id="a864a-117">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="a864a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a864a-118">-DefaultProfile</span></span>
<span data-ttu-id="a864a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a864a-120">-위치</span><span class="sxs-lookup"><span data-stu-id="a864a-120">-Location</span></span>
<span data-ttu-id="a864a-121">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-121">Specifies a location.</span></span>

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

### <span data-ttu-id="a864a-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="a864a-122">-OsDisk</span></span>
<span data-ttu-id="a864a-123">운영 체제 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="a864a-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a864a-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="a864a-125">원본 가상 컴퓨터 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="a864a-126">태그</span><span class="sxs-lookup"><span data-stu-id="a864a-126">-Tag</span></span>
<span data-ttu-id="a864a-127">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a864a-128">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a864a-128">For example:</span></span>

<span data-ttu-id="a864a-129">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a864a-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a864a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a864a-130">-Confirm</span></span>
<span data-ttu-id="a864a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a864a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a864a-132">-WhatIf</span></span>
<span data-ttu-id="a864a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a864a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a864a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a864a-135">CommonParameters</span></span>
<span data-ttu-id="a864a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a864a-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a864a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a864a-138">입력</span><span class="sxs-lookup"><span data-stu-id="a864a-138">INPUTS</span></span>

### <span data-ttu-id="a864a-139">않아야</span><span class="sxs-lookup"><span data-stu-id="a864a-139">None</span></span>
<span data-ttu-id="a864a-140">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a864a-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a864a-141">출력</span><span class="sxs-lookup"><span data-stu-id="a864a-141">OUTPUTS</span></span>

### <span data-ttu-id="a864a-142">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="a864a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a864a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a864a-143">NOTES</span></span>

## <span data-ttu-id="a864a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a864a-144">RELATED LINKS</span></span>

