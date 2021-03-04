---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 16a2250941ba0e28d40648ed2cd69fee7ffefc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955147"
---
# <span data-ttu-id="bbedb-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bbedb-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="bbedb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbedb-102">SYNOPSIS</span></span>
<span data-ttu-id="bbedb-103">Managed Instance에 대한 Azure AD SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="bbedb-104">구문</span><span class="sxs-lookup"><span data-stu-id="bbedb-104">SYNTAX</span></span>

### <span data-ttu-id="bbedb-105">UseResourceGroupAndInstanceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bbedb-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbedb-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbedb-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbedb-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbedb-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbedb-108">설명</span><span class="sxs-lookup"><span data-stu-id="bbedb-108">DESCRIPTION</span></span>
<span data-ttu-id="bbedb-109">**Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Managed Instance에 대한 Azure AD(Azure Active Directory) 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="bbedb-110">예제</span><span class="sxs-lookup"><span data-stu-id="bbedb-110">EXAMPLES</span></span>

### <span data-ttu-id="bbedb-111">예제 1: 관리자 제거</span><span class="sxs-lookup"><span data-stu-id="bbedb-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bbedb-112">이 명령은 리소스 그룹 ResourceGroup01과 연결된 ManagedInstanceName01이라는 관리 인스턴스에 대한 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="bbedb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="bbedb-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bbedb-114">이 명령은 관리되는 인스턴스 개체에서 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="bbedb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="bbedb-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bbedb-116">이 명령은 관리되는 인스턴스 리소스 식별자를 사용하여 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="bbedb-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bbedb-117">PARAMETERS</span></span>

### <span data-ttu-id="bbedb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbedb-118">-DefaultProfile</span></span>
<span data-ttu-id="bbedb-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbedb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bbedb-120">-Force</span></span>
<span data-ttu-id="bbedb-121">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="bbedb-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bbedb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbedb-122">-InputObject</span></span>
<span data-ttu-id="bbedb-123">사용할 관리되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-123">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbedb-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bbedb-124">-InstanceName</span></span>
<span data-ttu-id="bbedb-125">SQL 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-125">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbedb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbedb-126">-PassThru</span></span>
<span data-ttu-id="bbedb-127">제거된 AD 관리자를 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="bbedb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbedb-128">-ResourceGroupName</span></span>
<span data-ttu-id="bbedb-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbedb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbedb-130">-ResourceId</span></span>
<span data-ttu-id="bbedb-131">사용할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bbedb-131">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbedb-132">-확인</span><span class="sxs-lookup"><span data-stu-id="bbedb-132">-Confirm</span></span>
<span data-ttu-id="bbedb-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbedb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbedb-134">-WhatIf</span></span>
<span data-ttu-id="bbedb-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbedb-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbedb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbedb-137">CommonParameters</span></span>
<span data-ttu-id="bbedb-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bbedb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbedb-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbedb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbedb-140">입력</span><span class="sxs-lookup"><span data-stu-id="bbedb-140">INPUTS</span></span>

### <span data-ttu-id="bbedb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bbedb-141">System.String</span></span>

## <span data-ttu-id="bbedb-142">출력</span><span class="sxs-lookup"><span data-stu-id="bbedb-142">OUTPUTS</span></span>

### <span data-ttu-id="bbedb-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="bbedb-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="bbedb-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bbedb-144">NOTES</span></span>

## <span data-ttu-id="bbedb-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbedb-145">RELATED LINKS</span></span>

[<span data-ttu-id="bbedb-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bbedb-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="bbedb-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bbedb-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
