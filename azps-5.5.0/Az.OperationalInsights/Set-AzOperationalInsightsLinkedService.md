---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186708"
---
# <span data-ttu-id="f3e56-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="f3e56-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="f3e56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3e56-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e56-103">작업 영역의 연결 서비스</span><span class="sxs-lookup"><span data-stu-id="f3e56-103">link service for workspace</span></span>

## <span data-ttu-id="f3e56-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3e56-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3e56-105">설명</span><span class="sxs-lookup"><span data-stu-id="f3e56-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e56-106">작업 영역의 연결 서비스</span><span class="sxs-lookup"><span data-stu-id="f3e56-106">link service for workspace</span></span>

## <span data-ttu-id="f3e56-107">예제</span><span class="sxs-lookup"><span data-stu-id="f3e56-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e56-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3e56-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="f3e56-109">작업 영역의 클러스터 연결</span><span class="sxs-lookup"><span data-stu-id="f3e56-109">link cluster for workspace</span></span>

## <span data-ttu-id="f3e56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3e56-110">PARAMETERS</span></span>

### <span data-ttu-id="f3e56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3e56-111">-AsJob</span></span>
<span data-ttu-id="f3e56-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f3e56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3e56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e56-113">-DefaultProfile</span></span>
<span data-ttu-id="f3e56-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="f3e56-115">-LinkedServiceName</span></span>
<span data-ttu-id="f3e56-116">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e56-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3e56-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3e56-119">-ResourceId</span></span>
<span data-ttu-id="f3e56-120">작업 영역으로 연결될 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="f3e56-121">읽기 액세스가 필요한 리소스를 연결하는 데 사용</span><span class="sxs-lookup"><span data-stu-id="f3e56-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-122">-Tags</span><span class="sxs-lookup"><span data-stu-id="f3e56-122">-Tags</span></span>
<span data-ttu-id="f3e56-123">태그.</span><span class="sxs-lookup"><span data-stu-id="f3e56-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3e56-124">-WorkspaceName</span></span>
<span data-ttu-id="f3e56-125">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="f3e56-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="f3e56-127">작업 영역으로 연결될 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="f3e56-128">쓰기 액세스가 필요한 리소스를 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="f3e56-129">클러스터에는 프로비전 상태 "Succeeded" 및 유효한 키vault 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e56-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3e56-130">-Confirm</span></span>
<span data-ttu-id="f3e56-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3e56-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e56-132">-WhatIf</span></span>
<span data-ttu-id="f3e56-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f3e56-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3e56-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3e56-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e56-135">CommonParameters</span></span>
<span data-ttu-id="f3e56-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e56-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e56-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3e56-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e56-138">입력</span><span class="sxs-lookup"><span data-stu-id="f3e56-138">INPUTS</span></span>

### <span data-ttu-id="f3e56-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f3e56-139">System.String</span></span>

## <span data-ttu-id="f3e56-140">출력</span><span class="sxs-lookup"><span data-stu-id="f3e56-140">OUTPUTS</span></span>

### <span data-ttu-id="f3e56-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f3e56-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="f3e56-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3e56-142">NOTES</span></span>

## <span data-ttu-id="f3e56-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3e56-143">RELATED LINKS</span></span>
