---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: a8985d77ba1bbf33e49f353ad39d287f7bd3979b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955152"
---
# <span data-ttu-id="d104c-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d104c-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="d104c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d104c-102">SYNOPSIS</span></span>
<span data-ttu-id="d104c-103">관리되는 데이터베이스 SQL Azure를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="d104c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d104c-104">SYNTAX</span></span>

### <span data-ttu-id="d104c-105">RemoveInstanceFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="d104c-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d104c-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d104c-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d104c-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d104c-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d104c-108">설명</span><span class="sxs-lookup"><span data-stu-id="d104c-108">DESCRIPTION</span></span>
<span data-ttu-id="d104c-109">**Remove-AzSqlInstance** cmdlet은 Azure 데이터베이스 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d104c-110">예제</span><span class="sxs-lookup"><span data-stu-id="d104c-110">EXAMPLES</span></span>

### <span data-ttu-id="d104c-111">예제 1: 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="d104c-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d104c-112">이 명령은 managedInstance1이라는 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="d104c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d104c-113">PARAMETERS</span></span>

### <span data-ttu-id="d104c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d104c-114">-DefaultProfile</span></span>
<span data-ttu-id="d104c-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d104c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d104c-116">-Force</span></span>
<span data-ttu-id="d104c-117">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="d104c-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d104c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d104c-118">-InputObject</span></span>
<span data-ttu-id="d104c-119">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="d104c-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d104c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d104c-120">-Name</span></span>
<span data-ttu-id="d104c-121">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d104c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d104c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d104c-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d104c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d104c-124">-ResourceId</span></span>
<span data-ttu-id="d104c-125">제거할 인스턴스 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d104c-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d104c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d104c-126">-Confirm</span></span>
<span data-ttu-id="d104c-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d104c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d104c-128">-WhatIf</span></span>
<span data-ttu-id="d104c-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d104c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d104c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d104c-131">CommonParameters</span></span>
<span data-ttu-id="d104c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d104c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d104c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d104c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d104c-134">입력</span><span class="sxs-lookup"><span data-stu-id="d104c-134">INPUTS</span></span>

### <span data-ttu-id="d104c-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d104c-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d104c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d104c-136">System.String</span></span>

## <span data-ttu-id="d104c-137">출력</span><span class="sxs-lookup"><span data-stu-id="d104c-137">OUTPUTS</span></span>

### <span data-ttu-id="d104c-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d104c-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d104c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d104c-139">NOTES</span></span>

## <span data-ttu-id="d104c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d104c-140">RELATED LINKS</span></span>
