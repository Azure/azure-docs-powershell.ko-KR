---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: e92d167b235c84f5f5e3a6aaa79c4af745158b72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532083"
---
# <span data-ttu-id="745f6-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="745f6-101">New-AzureRmImage</span></span>

## <span data-ttu-id="745f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="745f6-102">SYNOPSIS</span></span>
<span data-ttu-id="745f6-103">이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="745f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="745f6-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="745f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="745f6-105">DESCRIPTION</span></span>
<span data-ttu-id="745f6-106">**AzureRmImage** cmdlet은 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="745f6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="745f6-107">EXAMPLES</span></span>

### <span data-ttu-id="745f6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="745f6-108">Example 1</span></span>
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

<span data-ttu-id="745f6-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="745f6-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="745f6-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="745f6-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="745f6-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="745f6-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="745f6-115">변수</span><span class="sxs-lookup"><span data-stu-id="745f6-115">PARAMETERS</span></span>

### <span data-ttu-id="745f6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="745f6-116">-AsJob</span></span>
<span data-ttu-id="745f6-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="745f6-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745f6-118">-DefaultProfile</span></span>
<span data-ttu-id="745f6-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="745f6-120">-이미지</span><span class="sxs-lookup"><span data-stu-id="745f6-120">-Image</span></span>
<span data-ttu-id="745f6-121">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="745f6-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="745f6-122">-ImageName</span></span>
<span data-ttu-id="745f6-123">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="745f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="745f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="745f6-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="745f6-126">-확인</span><span class="sxs-lookup"><span data-stu-id="745f6-126">-Confirm</span></span>
<span data-ttu-id="745f6-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="745f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="745f6-128">-WhatIf</span></span>
<span data-ttu-id="745f6-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="745f6-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="745f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745f6-131">CommonParameters</span></span>
<span data-ttu-id="745f6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="745f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745f6-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745f6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745f6-134">입력</span><span class="sxs-lookup"><span data-stu-id="745f6-134">INPUTS</span></span>

### <span data-ttu-id="745f6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="745f6-135">System.String</span></span>

### <span data-ttu-id="745f6-136">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="745f6-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="745f6-137">매개 변수: Image (ByValue)</span><span class="sxs-lookup"><span data-stu-id="745f6-137">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="745f6-138">출력</span><span class="sxs-lookup"><span data-stu-id="745f6-138">OUTPUTS</span></span>

### <span data-ttu-id="745f6-139">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="745f6-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="745f6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="745f6-140">NOTES</span></span>

## <span data-ttu-id="745f6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="745f6-141">RELATED LINKS</span></span>
