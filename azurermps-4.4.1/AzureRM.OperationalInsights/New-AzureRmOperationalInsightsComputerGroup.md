---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 8a54a735b41ef537a31f5e3e1ce2789d10e60af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530738"
---
# <span data-ttu-id="dcd8a-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="dcd8a-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="dcd8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd8a-103">컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dcd8a-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd8a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dcd8a-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd8a-106">**AzureRmOperationalInsightsComputerGroup** cmdlet은 리소스 그룹 및 위치에 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="dcd8a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dcd8a-107">EXAMPLES</span></span>

## <span data-ttu-id="dcd8a-108">변수</span><span class="sxs-lookup"><span data-stu-id="dcd8a-108">PARAMETERS</span></span>

### <span data-ttu-id="dcd8a-109">-범주</span><span class="sxs-lookup"><span data-stu-id="dcd8a-109">-Category</span></span>
<span data-ttu-id="dcd8a-110">컴퓨터 그룹의 범주를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dcd8a-111">-DisplayName</span></span>
<span data-ttu-id="dcd8a-112">컴퓨터 그룹의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-112">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dcd8a-113">-Force</span></span>
<span data-ttu-id="dcd8a-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcd8a-115">-쿼리</span><span class="sxs-lookup"><span data-stu-id="dcd8a-115">-Query</span></span>
<span data-ttu-id="dcd8a-116">컴퓨터 그룹의 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-116">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd8a-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcd8a-118">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-118">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dcd8a-119">Cmdlet이이 리소스 그룹에 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-119">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-120">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="dcd8a-120">-SavedSearchId</span></span>
<span data-ttu-id="dcd8a-121">컴퓨터 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-121">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-122">-버전</span><span class="sxs-lookup"><span data-stu-id="dcd8a-122">-Version</span></span>
<span data-ttu-id="dcd8a-123">버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-123">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dcd8a-124">-WorkspaceName</span></span>
<span data-ttu-id="dcd8a-125">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-126">-확인</span><span class="sxs-lookup"><span data-stu-id="dcd8a-126">-Confirm</span></span>
<span data-ttu-id="dcd8a-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd8a-128">-WhatIf</span></span>
<span data-ttu-id="dcd8a-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd8a-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd8a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd8a-131">-DefaultProfile</span></span>
<span data-ttu-id="dcd8a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcd8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd8a-133">CommonParameters</span></span>
<span data-ttu-id="dcd8a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd8a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd8a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd8a-136">입력</span><span class="sxs-lookup"><span data-stu-id="dcd8a-136">INPUTS</span></span>

## <span data-ttu-id="dcd8a-137">출력</span><span class="sxs-lookup"><span data-stu-id="dcd8a-137">OUTPUTS</span></span>

## <span data-ttu-id="dcd8a-138">상속자</span><span class="sxs-lookup"><span data-stu-id="dcd8a-138">NOTES</span></span>

## <span data-ttu-id="dcd8a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcd8a-139">RELATED LINKS</span></span>

