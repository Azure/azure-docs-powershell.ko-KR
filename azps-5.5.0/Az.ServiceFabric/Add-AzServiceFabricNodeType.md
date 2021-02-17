---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208080"
---
# <span data-ttu-id="aaa75-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="aaa75-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="aaa75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaa75-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa75-103">기존 클러스터에 새 노드 유형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="aaa75-104">구문</span><span class="sxs-lookup"><span data-stu-id="aaa75-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa75-105">설명</span><span class="sxs-lookup"><span data-stu-id="aaa75-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa75-106">기존 클러스터에 새 노드 형식을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="aaa75-107">예제</span><span class="sxs-lookup"><span data-stu-id="aaa75-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aaa75-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="aaa75-109">이 명령은 용량이 5인 새 NodeType 'n2'를 추가하고 vm 관리자 이름은 'adminName'입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="aaa75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaa75-110">PARAMETERS</span></span>

### <span data-ttu-id="aaa75-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="aaa75-111">-Capacity</span></span>
<span data-ttu-id="aaa75-112">용량</span><span class="sxs-lookup"><span data-stu-id="aaa75-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa75-113">-DefaultProfile</span></span>
<span data-ttu-id="aaa75-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaa75-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="aaa75-115">-DurabilityLevel</span></span>
<span data-ttu-id="aaa75-116">NodeType의 내구성 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aaa75-117">-Name</span></span>
<span data-ttu-id="aaa75-118">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="aaa75-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="aaa75-119">-NodeType</span></span>
<span data-ttu-id="aaa75-120">노드 유형 이름</span><span class="sxs-lookup"><span data-stu-id="aaa75-120">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa75-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaa75-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="aaa75-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="aaa75-123">-Tier</span></span>
<span data-ttu-id="aaa75-124">Vm SKU 계층</span><span class="sxs-lookup"><span data-stu-id="aaa75-124">Vm Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="aaa75-125">-VmPassword</span></span>
<span data-ttu-id="aaa75-126">VM에 로그인하기 위한 암호</span><span class="sxs-lookup"><span data-stu-id="aaa75-126">The password for login to the Vm</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="aaa75-127">-VmSku</span></span>
<span data-ttu-id="aaa75-128">SKU 이름</span><span class="sxs-lookup"><span data-stu-id="aaa75-128">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="aaa75-129">-VmUserName</span></span>
<span data-ttu-id="aaa75-130">VM에 로깅하기 위한 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="aaa75-130">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa75-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaa75-131">-Confirm</span></span>
<span data-ttu-id="aaa75-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa75-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa75-133">-WhatIf</span></span>
<span data-ttu-id="aaa75-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aaa75-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa75-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa75-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa75-136">CommonParameters</span></span>
<span data-ttu-id="aaa75-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa75-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa75-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aaa75-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa75-139">입력</span><span class="sxs-lookup"><span data-stu-id="aaa75-139">INPUTS</span></span>

### <span data-ttu-id="aaa75-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aaa75-140">System.String</span></span>

### <span data-ttu-id="aaa75-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aaa75-141">System.Int32</span></span>

### <span data-ttu-id="aaa75-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="aaa75-142">System.Security.SecureString</span></span>

### <span data-ttu-id="aaa75-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="aaa75-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="aaa75-144">출력</span><span class="sxs-lookup"><span data-stu-id="aaa75-144">OUTPUTS</span></span>

### <span data-ttu-id="aaa75-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="aaa75-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="aaa75-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aaa75-146">NOTES</span></span>

## <span data-ttu-id="aaa75-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaa75-147">RELATED LINKS</span></span>
