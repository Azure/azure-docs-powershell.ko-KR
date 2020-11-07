---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 1a04ca9df307b8d6251c6a8378df86827a76d001
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875985"
---
# <span data-ttu-id="99d52-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="99d52-101">Update-AzImage</span></span>

## <span data-ttu-id="99d52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d52-102">SYNOPSIS</span></span>
<span data-ttu-id="99d52-103">이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-103">Updates an image.</span></span>

## <span data-ttu-id="99d52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99d52-104">SYNTAX</span></span>

```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99d52-105">DESCRIPTION</span></span>
<span data-ttu-id="99d52-106">**업데이트 AzImage** cmdlet은 이미지를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-106">The **Update-AzImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="99d52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99d52-107">EXAMPLES</span></span>

### <span data-ttu-id="99d52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="99d52-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="99d52-109">이 명령은 리소스 그룹 ' ResourceGroup01 '의 기존 이미지 ' Image01 '에서 논리 단위 번호 1의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="99d52-110">변수</span><span class="sxs-lookup"><span data-stu-id="99d52-110">PARAMETERS</span></span>

### <span data-ttu-id="99d52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99d52-111">-AsJob</span></span>
<span data-ttu-id="99d52-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="99d52-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d52-113">-DefaultProfile</span></span>
<span data-ttu-id="99d52-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d52-115">-이미지</span><span class="sxs-lookup"><span data-stu-id="99d52-115">-Image</span></span>
<span data-ttu-id="99d52-116">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-116">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99d52-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="99d52-117">-ImageName</span></span>
<span data-ttu-id="99d52-118">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d52-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d52-119">-ResourceGroupName</span></span>
<span data-ttu-id="99d52-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d52-121">-확인</span><span class="sxs-lookup"><span data-stu-id="99d52-121">-Confirm</span></span>
<span data-ttu-id="99d52-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d52-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d52-123">-WhatIf</span></span>
<span data-ttu-id="99d52-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d52-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d52-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d52-126">CommonParameters</span></span>
<span data-ttu-id="99d52-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d52-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d52-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d52-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d52-129">입력</span><span class="sxs-lookup"><span data-stu-id="99d52-129">INPUTS</span></span>

### <span data-ttu-id="99d52-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99d52-130">System.String</span></span>
<span data-ttu-id="99d52-131">PSImage의. m a.</span><span class="sxs-lookup"><span data-stu-id="99d52-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="99d52-132">출력</span><span class="sxs-lookup"><span data-stu-id="99d52-132">OUTPUTS</span></span>

### <span data-ttu-id="99d52-133">System. 개체</span><span class="sxs-lookup"><span data-stu-id="99d52-133">System.Object</span></span>

## <span data-ttu-id="99d52-134">상속자</span><span class="sxs-lookup"><span data-stu-id="99d52-134">NOTES</span></span>

## <span data-ttu-id="99d52-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99d52-135">RELATED LINKS</span></span>

