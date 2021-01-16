---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322650"
---
# <span data-ttu-id="33fdd-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="33fdd-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="33fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="33fdd-103">가상 클러스터에서 Azure SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="33fdd-104">구문</span><span class="sxs-lookup"><span data-stu-id="33fdd-104">SYNTAX</span></span>

### <span data-ttu-id="33fdd-105">RemoveVirtualClusterFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="33fdd-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33fdd-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="33fdd-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33fdd-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="33fdd-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33fdd-108">설명</span><span class="sxs-lookup"><span data-stu-id="33fdd-108">DESCRIPTION</span></span>
<span data-ttu-id="33fdd-109">**Remove-AzSqlVirtualCluster** cmdlet은 Azure SQL Virtual Cluster를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="33fdd-110">예제</span><span class="sxs-lookup"><span data-stu-id="33fdd-110">EXAMPLES</span></span>

### <span data-ttu-id="33fdd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="33fdd-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="33fdd-112">이 명령은 리소스 그룹 ResourceGroup01에 할당된 VirtualCluster1이라는 가상 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="33fdd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33fdd-113">PARAMETERS</span></span>

### <span data-ttu-id="33fdd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33fdd-114">-AsJob</span></span>
<span data-ttu-id="33fdd-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33fdd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33fdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fdd-116">-DefaultProfile</span></span>
<span data-ttu-id="33fdd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33fdd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33fdd-118">-InputObject</span></span>
<span data-ttu-id="33fdd-119">제거할 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="33fdd-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33fdd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="33fdd-120">-Name</span></span>
<span data-ttu-id="33fdd-121">가상 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fdd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33fdd-122">-ResourceGroupName</span></span>
<span data-ttu-id="33fdd-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fdd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33fdd-124">-ResourceId</span></span>
<span data-ttu-id="33fdd-125">제거할 인스턴스 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="33fdd-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fdd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33fdd-126">-Confirm</span></span>
<span data-ttu-id="33fdd-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33fdd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33fdd-128">-WhatIf</span></span>
<span data-ttu-id="33fdd-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="33fdd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33fdd-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33fdd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fdd-131">CommonParameters</span></span>
<span data-ttu-id="33fdd-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33fdd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fdd-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33fdd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fdd-134">입력</span><span class="sxs-lookup"><span data-stu-id="33fdd-134">INPUTS</span></span>

### <span data-ttu-id="33fdd-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="33fdd-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="33fdd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="33fdd-136">System.String</span></span>

## <span data-ttu-id="33fdd-137">출력</span><span class="sxs-lookup"><span data-stu-id="33fdd-137">OUTPUTS</span></span>

### <span data-ttu-id="33fdd-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="33fdd-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="33fdd-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33fdd-139">NOTES</span></span>

## <span data-ttu-id="33fdd-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33fdd-140">RELATED LINKS</span></span>
