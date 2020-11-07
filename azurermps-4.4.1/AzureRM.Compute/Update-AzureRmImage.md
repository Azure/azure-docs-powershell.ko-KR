---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: ccca83cdbebcf73df9059807dc5b030e4ab21736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703124"
---
# <span data-ttu-id="7d8c4-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="7d8c4-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="7d8c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8c4-103">이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d8c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d8c4-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7d8c4-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8c4-106">**업데이트 AzureRmImage** cmdlet은 이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="7d8c4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7d8c4-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d8c4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="7d8c4-109">이 명령은 리소스 그룹 ' ResourceGroup01 '의 기존 이미지 ' Image01 '에서 논리 단위 번호 1의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7d8c4-110">변수</span><span class="sxs-lookup"><span data-stu-id="7d8c4-110">PARAMETERS</span></span>

### <span data-ttu-id="7d8c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8c4-111">-DefaultProfile</span></span>
<span data-ttu-id="7d8c4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8c4-113">-이미지</span><span class="sxs-lookup"><span data-stu-id="7d8c4-113">-Image</span></span>
<span data-ttu-id="7d8c4-114">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="7d8c4-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7d8c4-115">-ImageName</span></span>
<span data-ttu-id="7d8c4-116">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-116">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="7d8c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d8c4-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7d8c4-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7d8c4-119">-Confirm</span></span>
<span data-ttu-id="7d8c4-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8c4-121">-WhatIf</span></span>
<span data-ttu-id="7d8c4-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8c4-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8c4-124">CommonParameters</span></span>
<span data-ttu-id="7d8c4-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8c4-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8c4-127">입력</span><span class="sxs-lookup"><span data-stu-id="7d8c4-127">INPUTS</span></span>

### <span data-ttu-id="7d8c4-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d8c4-128">System.String</span></span>
<span data-ttu-id="7d8c4-129">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="7d8c4-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="7d8c4-130">출력</span><span class="sxs-lookup"><span data-stu-id="7d8c4-130">OUTPUTS</span></span>

### <span data-ttu-id="7d8c4-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="7d8c4-131">System.Object</span></span>

## <span data-ttu-id="7d8c4-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7d8c4-132">NOTES</span></span>

## <span data-ttu-id="7d8c4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d8c4-133">RELATED LINKS</span></span>

