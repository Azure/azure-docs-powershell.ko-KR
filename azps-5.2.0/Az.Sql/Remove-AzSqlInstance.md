---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369636"
---
# <span data-ttu-id="7e3f7-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7e3f7-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="7e3f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3f7-103">Azure SQL Managed Database 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="7e3f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e3f7-104">SYNTAX</span></span>

### <span data-ttu-id="7e3f7-105">RemoveInstanceFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e3f7-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e3f7-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="7e3f7-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e3f7-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="7e3f7-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e3f7-108">설명</span><span class="sxs-lookup"><span data-stu-id="7e3f7-108">DESCRIPTION</span></span>
<span data-ttu-id="7e3f7-109">**Remove-AzSqlInstance** cmdlet은 Azure SQL Managed Instance를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="7e3f7-110">예제</span><span class="sxs-lookup"><span data-stu-id="7e3f7-110">EXAMPLES</span></span>

### <span data-ttu-id="7e3f7-111">예제 1: 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="7e3f7-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7e3f7-112">이 명령은 managedInstance1이라는 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="7e3f7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e3f7-113">PARAMETERS</span></span>

### <span data-ttu-id="7e3f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3f7-114">-DefaultProfile</span></span>
<span data-ttu-id="7e3f7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e3f7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7e3f7-116">-Force</span></span>
<span data-ttu-id="7e3f7-117">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="7e3f7-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7e3f7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e3f7-118">-InputObject</span></span>
<span data-ttu-id="7e3f7-119">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="7e3f7-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="7e3f7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7e3f7-120">-Name</span></span>
<span data-ttu-id="7e3f7-121">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-121">SQL instance name.</span></span>

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

### <span data-ttu-id="7e3f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e3f7-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e3f7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e3f7-124">-ResourceId</span></span>
<span data-ttu-id="7e3f7-125">제거할 인스턴스 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7e3f7-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="7e3f7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e3f7-126">-Confirm</span></span>
<span data-ttu-id="7e3f7-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3f7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3f7-128">-WhatIf</span></span>
<span data-ttu-id="7e3f7-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e3f7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3f7-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3f7-131">CommonParameters</span></span>
<span data-ttu-id="7e3f7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3f7-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e3f7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3f7-134">입력</span><span class="sxs-lookup"><span data-stu-id="7e3f7-134">INPUTS</span></span>

### <span data-ttu-id="7e3f7-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7e3f7-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="7e3f7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7e3f7-136">System.String</span></span>

## <span data-ttu-id="7e3f7-137">출력</span><span class="sxs-lookup"><span data-stu-id="7e3f7-137">OUTPUTS</span></span>

### <span data-ttu-id="7e3f7-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7e3f7-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7e3f7-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e3f7-139">NOTES</span></span>

## <span data-ttu-id="7e3f7-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e3f7-140">RELATED LINKS</span></span>
