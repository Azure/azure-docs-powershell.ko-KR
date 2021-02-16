---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195948"
---
# <span data-ttu-id="057a6-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="057a6-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="057a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="057a6-102">SYNOPSIS</span></span>
<span data-ttu-id="057a6-103">Managed Instance에 대한 Azure AD SQL 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="057a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="057a6-104">SYNTAX</span></span>

### <span data-ttu-id="057a6-105">UseResourceGroupAndInstanceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="057a6-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057a6-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="057a6-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="057a6-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="057a6-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="057a6-108">설명</span><span class="sxs-lookup"><span data-stu-id="057a6-108">DESCRIPTION</span></span>
<span data-ttu-id="057a6-109">**Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Managed Instance에 대한 Azure AD(Azure Active Directory) 관리자를 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="057a6-110">한 번의 관리자만 프로비전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="057a6-111">Azure AD의 다음 멤버는 Managed Instance 관리자로 SQL 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="057a6-112">Azure AD의 네이티브 멤버</span><span class="sxs-lookup"><span data-stu-id="057a6-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="057a6-113">Azure AD의 페더리된 멤버</span><span class="sxs-lookup"><span data-stu-id="057a6-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="057a6-114">다른 Azure AD에서 보안 그룹으로 만든 Azure AD 그룹은 관리자 권한으로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="057a6-115">Outlook.com, Hotmail.com 또는 Live.com 도메인과 같은 Microsoft 계정은 관리자로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="057a6-116">다른 게스트 계정(예: Gmail.com 또는 Yahoo.com 도메인)은 관리자로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="057a6-117">관리자 권한으로 전용 Azure AD 그룹을 프로비전하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="057a6-118">예제</span><span class="sxs-lookup"><span data-stu-id="057a6-118">EXAMPLES</span></span>

### <span data-ttu-id="057a6-119">예제 1: 리소스 그룹과 연결된 관리되는 인스턴스에 대한 관리자 그룹 프로비전</span><span class="sxs-lookup"><span data-stu-id="057a6-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="057a6-120">이 명령은 ManagedInstance01이라는 관리되는 인스턴스에 대해 DBAS라는 Azure AD 관리자 그룹을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="057a6-121">이 서버는 리소스 그룹 ResourceGroup01과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="057a6-122">예제 2: 관리되는 인스턴스 개체를 사용하여 관리자 사용자 프로비전</span><span class="sxs-lookup"><span data-stu-id="057a6-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="057a6-123">이 명령은 Azure AD 사용자를 관리되는 인스턴스 개체의 관리자로 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="057a6-124">예제 3: 관리되는 인스턴스 리소스 식별자를 사용하여 관리자 프로비전</span><span class="sxs-lookup"><span data-stu-id="057a6-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="057a6-125">이 명령은 관리되는 인스턴스 리소스 식별자를 사용하여 관리자로 Azure AD 사용자를 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="057a6-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="057a6-126">PARAMETERS</span></span>

### <span data-ttu-id="057a6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057a6-127">-DefaultProfile</span></span>
<span data-ttu-id="057a6-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="057a6-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="057a6-129">-DisplayName</span></span>
<span data-ttu-id="057a6-130">권한을 부여할 사용자 또는 그룹의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="057a6-131">이 표시 이름은 현재 구독과 연결된 Active Directory에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="057a6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="057a6-132">-InputObject</span></span>
<span data-ttu-id="057a6-133">사용할 관리되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="057a6-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="057a6-134">-InstanceName</span></span>
<span data-ttu-id="057a6-135">SQL 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="057a6-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="057a6-136">-ObjectId</span></span>
<span data-ttu-id="057a6-137">권한을 부여할 Azure Active Directory에서 사용자 또는 그룹의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="057a6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057a6-138">-ResourceGroupName</span></span>
<span data-ttu-id="057a6-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="057a6-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="057a6-140">-ResourceId</span></span>
<span data-ttu-id="057a6-141">사용할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="057a6-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="057a6-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="057a6-142">-Confirm</span></span>
<span data-ttu-id="057a6-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="057a6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="057a6-144">-WhatIf</span></span>
<span data-ttu-id="057a6-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="057a6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="057a6-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="057a6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057a6-147">CommonParameters</span></span>
<span data-ttu-id="057a6-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="057a6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057a6-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="057a6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057a6-150">입력</span><span class="sxs-lookup"><span data-stu-id="057a6-150">INPUTS</span></span>

### <span data-ttu-id="057a6-151">System.String</span><span class="sxs-lookup"><span data-stu-id="057a6-151">System.String</span></span>

### <span data-ttu-id="057a6-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="057a6-152">System.Guid</span></span>

## <span data-ttu-id="057a6-153">출력</span><span class="sxs-lookup"><span data-stu-id="057a6-153">OUTPUTS</span></span>

### <span data-ttu-id="057a6-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="057a6-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="057a6-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="057a6-155">NOTES</span></span>

## <span data-ttu-id="057a6-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="057a6-156">RELATED LINKS</span></span>

[<span data-ttu-id="057a6-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="057a6-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="057a6-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="057a6-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
