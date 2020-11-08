---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056818"
---
# <span data-ttu-id="b231c-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b231c-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="b231c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b231c-102">SYNOPSIS</span></span>
<span data-ttu-id="b231c-103">Application insights 연결 된 저장소 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="b231c-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="b231c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b231c-104">SYNTAX</span></span>

### <span data-ttu-id="b231c-105">ByResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b231c-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b231c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b231c-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b231c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b231c-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b231c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b231c-108">DESCRIPTION</span></span>
<span data-ttu-id="b231c-109">Application insights 연결 된 저장소 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="b231c-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="b231c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b231c-110">EXAMPLES</span></span>

### <span data-ttu-id="b231c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b231c-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="b231c-112">"ComponentName" 구성 요소에서 연결 된 저장소 계정을 업데이트 하 여 $account에 연결</span><span class="sxs-lookup"><span data-stu-id="b231c-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="b231c-113">변수</span><span class="sxs-lookup"><span data-stu-id="b231c-113">PARAMETERS</span></span>

### <span data-ttu-id="b231c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="b231c-114">-ComponentName</span></span>
<span data-ttu-id="b231c-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="b231c-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b231c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b231c-116">-DefaultProfile</span></span>
<span data-ttu-id="b231c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b231c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b231c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b231c-118">-InputObject</span></span>
<span data-ttu-id="b231c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b231c-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b231c-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="b231c-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="b231c-121">저장소 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="b231c-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b231c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b231c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b231c-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b231c-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b231c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b231c-124">-ResourceId</span></span>
<span data-ttu-id="b231c-125">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="b231c-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b231c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="b231c-126">-Confirm</span></span>
<span data-ttu-id="b231c-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b231c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b231c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b231c-128">-WhatIf</span></span>
<span data-ttu-id="b231c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b231c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b231c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b231c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b231c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b231c-131">CommonParameters</span></span>
<span data-ttu-id="b231c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b231c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b231c-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b231c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b231c-134">입력</span><span class="sxs-lookup"><span data-stu-id="b231c-134">INPUTS</span></span>

### <span data-ttu-id="b231c-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b231c-135">System.String</span></span>

### <span data-ttu-id="b231c-136">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b231c-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="b231c-137">출력</span><span class="sxs-lookup"><span data-stu-id="b231c-137">OUTPUTS</span></span>

### <span data-ttu-id="b231c-138">PSComponentLinkedStorageAccounts-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b231c-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="b231c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b231c-139">NOTES</span></span>

## <span data-ttu-id="b231c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b231c-140">RELATED LINKS</span></span>
