---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226437"
---
# <span data-ttu-id="cad69-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cad69-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="cad69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cad69-102">SYNOPSIS</span></span>
<span data-ttu-id="cad69-103">Application insights 연결 된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="cad69-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="cad69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cad69-104">SYNTAX</span></span>

### <span data-ttu-id="cad69-105">ByResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cad69-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad69-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad69-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad69-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad69-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad69-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cad69-108">DESCRIPTION</span></span>
<span data-ttu-id="cad69-109">Application insights 연결 된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="cad69-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="cad69-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cad69-110">EXAMPLES</span></span>

### <span data-ttu-id="cad69-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cad69-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="cad69-112">Application insights 구성 요소 "componentName"와 연결 된 연결 된 저장소 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="cad69-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="cad69-113">변수</span><span class="sxs-lookup"><span data-stu-id="cad69-113">PARAMETERS</span></span>

### <span data-ttu-id="cad69-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="cad69-114">-ComponentName</span></span>
<span data-ttu-id="cad69-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="cad69-115">Component Name</span></span>

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

### <span data-ttu-id="cad69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad69-116">-DefaultProfile</span></span>
<span data-ttu-id="cad69-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cad69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cad69-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cad69-118">-InputObject</span></span>
<span data-ttu-id="cad69-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cad69-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="cad69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad69-120">-ResourceGroupName</span></span>
<span data-ttu-id="cad69-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cad69-121">Resource Group Name</span></span>

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

### <span data-ttu-id="cad69-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cad69-122">-ResourceId</span></span>
<span data-ttu-id="cad69-123">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="cad69-123">Component ResourceId</span></span>

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

### <span data-ttu-id="cad69-124">-확인</span><span class="sxs-lookup"><span data-stu-id="cad69-124">-Confirm</span></span>
<span data-ttu-id="cad69-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad69-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad69-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad69-126">-WhatIf</span></span>
<span data-ttu-id="cad69-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cad69-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cad69-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cad69-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad69-129">CommonParameters</span></span>
<span data-ttu-id="cad69-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cad69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad69-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cad69-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad69-132">입력</span><span class="sxs-lookup"><span data-stu-id="cad69-132">INPUTS</span></span>

### <span data-ttu-id="cad69-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cad69-133">System.String</span></span>

### <span data-ttu-id="cad69-134">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cad69-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="cad69-135">출력</span><span class="sxs-lookup"><span data-stu-id="cad69-135">OUTPUTS</span></span>

### <span data-ttu-id="cad69-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cad69-136">System.Boolean</span></span>

## <span data-ttu-id="cad69-137">상속자</span><span class="sxs-lookup"><span data-stu-id="cad69-137">NOTES</span></span>

## <span data-ttu-id="cad69-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cad69-138">RELATED LINKS</span></span>
