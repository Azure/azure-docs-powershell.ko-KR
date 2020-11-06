---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 999e9e5fd9f0b93e71b222f228b1575e0492073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535264"
---
# <span data-ttu-id="b5d18-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="b5d18-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="b5d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d18-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d18-103">컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5d18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5d18-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5d18-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d18-106">**AzureRmOperationalInsightsComputerGroup** cmdlet은 리소스 그룹 및 위치에 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="b5d18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5d18-107">EXAMPLES</span></span>

## <span data-ttu-id="b5d18-108">변수</span><span class="sxs-lookup"><span data-stu-id="b5d18-108">PARAMETERS</span></span>

### <span data-ttu-id="b5d18-109">-범주</span><span class="sxs-lookup"><span data-stu-id="b5d18-109">-Category</span></span>
<span data-ttu-id="b5d18-110">컴퓨터 그룹의 범주를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-110">Specifies the category of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d18-111">-DefaultProfile</span></span>
<span data-ttu-id="b5d18-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b5d18-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5d18-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b5d18-113">-DisplayName</span></span>
<span data-ttu-id="b5d18-114">컴퓨터 그룹의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="b5d18-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5d18-115">-Force</span></span>
<span data-ttu-id="b5d18-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5d18-117">-쿼리</span><span class="sxs-lookup"><span data-stu-id="b5d18-117">-Query</span></span>
<span data-ttu-id="b5d18-118">컴퓨터 그룹의 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-118">Specifies the query of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d18-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5d18-120">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b5d18-121">Cmdlet이이 리소스 그룹에 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="b5d18-122">-SavedSearchId</span></span>
<span data-ttu-id="b5d18-123">컴퓨터 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-124">-버전</span><span class="sxs-lookup"><span data-stu-id="b5d18-124">-Version</span></span>
<span data-ttu-id="b5d18-125">버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-125">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5d18-126">-WorkspaceName</span></span>
<span data-ttu-id="b5d18-127">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-127">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b5d18-128">-Confirm</span></span>
<span data-ttu-id="b5d18-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d18-130">-WhatIf</span></span>
<span data-ttu-id="b5d18-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d18-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d18-133">CommonParameters</span></span>
<span data-ttu-id="b5d18-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d18-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d18-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d18-136">입력</span><span class="sxs-lookup"><span data-stu-id="b5d18-136">INPUTS</span></span>

### <span data-ttu-id="b5d18-137">않아야</span><span class="sxs-lookup"><span data-stu-id="b5d18-137">None</span></span>
<span data-ttu-id="b5d18-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5d18-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5d18-139">출력</span><span class="sxs-lookup"><span data-stu-id="b5d18-139">OUTPUTS</span></span>

## <span data-ttu-id="b5d18-140">상속자</span><span class="sxs-lookup"><span data-stu-id="b5d18-140">NOTES</span></span>

## <span data-ttu-id="b5d18-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5d18-141">RELATED LINKS</span></span>

