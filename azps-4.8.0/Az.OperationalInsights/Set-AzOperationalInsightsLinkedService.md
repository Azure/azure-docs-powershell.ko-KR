---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048803"
---
# <span data-ttu-id="2c67f-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="2c67f-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="2c67f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c67f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c67f-103">작업 영역에 대 한 링크 서비스</span><span class="sxs-lookup"><span data-stu-id="2c67f-103">link service for workspace</span></span>

## <span data-ttu-id="2c67f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c67f-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c67f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2c67f-105">DESCRIPTION</span></span>
<span data-ttu-id="2c67f-106">작업 영역에 대 한 링크 서비스</span><span class="sxs-lookup"><span data-stu-id="2c67f-106">link service for workspace</span></span>

## <span data-ttu-id="2c67f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2c67f-107">EXAMPLES</span></span>

### <span data-ttu-id="2c67f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c67f-108">Example 1</span></span>
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

<span data-ttu-id="2c67f-109">작업 영역에 대 한 링크 클러스터</span><span class="sxs-lookup"><span data-stu-id="2c67f-109">link cluster for workspace</span></span>

## <span data-ttu-id="2c67f-110">변수</span><span class="sxs-lookup"><span data-stu-id="2c67f-110">PARAMETERS</span></span>

### <span data-ttu-id="2c67f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c67f-111">-AsJob</span></span>
<span data-ttu-id="2c67f-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2c67f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c67f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c67f-113">-DefaultProfile</span></span>
<span data-ttu-id="2c67f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c67f-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="2c67f-115">-LinkedServiceName</span></span>
<span data-ttu-id="2c67f-116">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-116">The Workspace name.</span></span>

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

### <span data-ttu-id="2c67f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c67f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c67f-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-118">The resource group name.</span></span>

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

### <span data-ttu-id="2c67f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c67f-119">-ResourceId</span></span>
<span data-ttu-id="2c67f-120">작업 영역에 연결 되는 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="2c67f-121">이는 읽기 권한이 필요한 리소스를 연결 하는 데 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="2c67f-122">태그</span><span class="sxs-lookup"><span data-stu-id="2c67f-122">-Tags</span></span>
<span data-ttu-id="2c67f-123">태그도.</span><span class="sxs-lookup"><span data-stu-id="2c67f-123">Tags.</span></span>

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

### <span data-ttu-id="2c67f-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c67f-124">-WorkspaceName</span></span>
<span data-ttu-id="2c67f-125">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-125">The Workspace name.</span></span>

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

### <span data-ttu-id="2c67f-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="2c67f-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="2c67f-127">작업 영역에 연결 되는 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="2c67f-128">이는 쓰기 액세스가 필요한 리소스를 연결 하는 데 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="2c67f-129">클러스터에는 프로비저닝 상태 "성공" 및 유효한 keyvault 속성이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="2c67f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2c67f-130">-Confirm</span></span>
<span data-ttu-id="2c67f-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c67f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c67f-132">-WhatIf</span></span>
<span data-ttu-id="2c67f-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c67f-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c67f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c67f-135">CommonParameters</span></span>
<span data-ttu-id="2c67f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c67f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c67f-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c67f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c67f-138">입력</span><span class="sxs-lookup"><span data-stu-id="2c67f-138">INPUTS</span></span>

### <span data-ttu-id="2c67f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c67f-139">System.String</span></span>

## <span data-ttu-id="2c67f-140">출력</span><span class="sxs-lookup"><span data-stu-id="2c67f-140">OUTPUTS</span></span>

### <span data-ttu-id="2c67f-141">OperationalInsights. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="2c67f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="2c67f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2c67f-142">NOTES</span></span>

## <span data-ttu-id="2c67f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c67f-143">RELATED LINKS</span></span>
