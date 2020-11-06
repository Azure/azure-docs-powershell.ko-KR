---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: a18fe089cba54f6cbf0d70469a17f2d8f797b2e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525672"
---
# <span data-ttu-id="467c7-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="467c7-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="467c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="467c7-102">SYNOPSIS</span></span>
<span data-ttu-id="467c7-103">구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="467c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="467c7-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="467c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="467c7-105">DESCRIPTION</span></span>
<span data-ttu-id="467c7-106">**AzureRmImageConfig** cmdlet은 구성 가능한 image 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="467c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="467c7-107">EXAMPLES</span></span>

### <span data-ttu-id="467c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="467c7-108">Example 1</span></span>
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

<span data-ttu-id="467c7-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="467c7-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="467c7-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="467c7-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="467c7-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="467c7-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="467c7-115">변수</span><span class="sxs-lookup"><span data-stu-id="467c7-115">PARAMETERS</span></span>

### <span data-ttu-id="467c7-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="467c7-116">-DataDisk</span></span>
<span data-ttu-id="467c7-117">데이터 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467c7-118">-DefaultProfile</span></span>
<span data-ttu-id="467c7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-120">-위치</span><span class="sxs-lookup"><span data-stu-id="467c7-120">-Location</span></span>
<span data-ttu-id="467c7-121">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-121">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="467c7-122">-OsDisk</span></span>
<span data-ttu-id="467c7-123">운영 체제 디스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-123">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="467c7-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="467c7-125">원본 가상 컴퓨터 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-125">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-126">태그</span><span class="sxs-lookup"><span data-stu-id="467c7-126">-Tag</span></span>
<span data-ttu-id="467c7-127">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-127">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-128">-확인</span><span class="sxs-lookup"><span data-stu-id="467c7-128">-Confirm</span></span>
<span data-ttu-id="467c7-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467c7-130">-WhatIf</span></span>
<span data-ttu-id="467c7-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="467c7-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="467c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467c7-133">CommonParameters</span></span>
<span data-ttu-id="467c7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="467c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467c7-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467c7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467c7-136">입력</span><span class="sxs-lookup"><span data-stu-id="467c7-136">INPUTS</span></span>

### <span data-ttu-id="467c7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="467c7-137">System.String</span></span>
<span data-ttu-id="467c7-138">System.webserver. ImageOSDisk. ImageDataDisk []을 (를) 대 한 모든. a.</span><span class="sxs-lookup"><span data-stu-id="467c7-138">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="467c7-139">출력</span><span class="sxs-lookup"><span data-stu-id="467c7-139">OUTPUTS</span></span>

### <span data-ttu-id="467c7-140">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="467c7-140">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="467c7-141">상속자</span><span class="sxs-lookup"><span data-stu-id="467c7-141">NOTES</span></span>

## <span data-ttu-id="467c7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="467c7-142">RELATED LINKS</span></span>

