---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213904"
---
# <span data-ttu-id="aa5f7-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa5f7-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="aa5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5f7-103">SQL 관리 인스턴스에 대 한 Azure AD 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="aa5f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa5f7-104">SYNTAX</span></span>

### <span data-ttu-id="aa5f7-105">UseResourceGroupAndInstanceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aa5f7-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5f7-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa5f7-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa5f7-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa5f7-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa5f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aa5f7-108">DESCRIPTION</span></span>
<span data-ttu-id="aa5f7-109">**AzSqlInstanceActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL 관리 되는 인스턴스의 azure AD (Active Directory) 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="aa5f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aa5f7-110">EXAMPLES</span></span>

### <span data-ttu-id="aa5f7-111">예제 1: 관리자 제거</span><span class="sxs-lookup"><span data-stu-id="aa5f7-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="aa5f7-112">이 명령은 리소스 그룹 ResourceGroup01와 연결 된 ManagedInstanceName01 이라는 관리 되는 인스턴스에 대 한 Azure AD 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="aa5f7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="aa5f7-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="aa5f7-114">이 명령은 관리 되는 인스턴스 개체에서 Azure AD 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="aa5f7-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="aa5f7-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="aa5f7-116">이 명령은 관리 되는 인스턴스 리소스 식별자를 사용 하 여 Azure AD 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="aa5f7-117">변수</span><span class="sxs-lookup"><span data-stu-id="aa5f7-117">PARAMETERS</span></span>

### <span data-ttu-id="aa5f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5f7-118">-DefaultProfile</span></span>
<span data-ttu-id="aa5f7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa5f7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="aa5f7-120">-Force</span></span>
<span data-ttu-id="aa5f7-121">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="aa5f7-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aa5f7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa5f7-122">-InputObject</span></span>
<span data-ttu-id="aa5f7-123">사용할 관리 되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="aa5f7-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aa5f7-124">-InstanceName</span></span>
<span data-ttu-id="aa5f7-125">SQL 관리 되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="aa5f7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa5f7-126">-PassThru</span></span>
<span data-ttu-id="aa5f7-127">제거 된 광고 관리자를 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="aa5f7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa5f7-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa5f7-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa5f7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa5f7-130">-ResourceId</span></span>
<span data-ttu-id="aa5f7-131">사용할 인스턴스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="aa5f7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="aa5f7-132">-Confirm</span></span>
<span data-ttu-id="aa5f7-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa5f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa5f7-134">-WhatIf</span></span>
<span data-ttu-id="aa5f7-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa5f7-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa5f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5f7-137">CommonParameters</span></span>
<span data-ttu-id="aa5f7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5f7-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa5f7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5f7-140">입력</span><span class="sxs-lookup"><span data-stu-id="aa5f7-140">INPUTS</span></span>

### <span data-ttu-id="aa5f7-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa5f7-141">System.String</span></span>

## <span data-ttu-id="aa5f7-142">출력</span><span class="sxs-lookup"><span data-stu-id="aa5f7-142">OUTPUTS</span></span>

### <span data-ttu-id="aa5f7-143">InstanceActiveDirectoryAdministrator. AzureSqlInstanceActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="aa5f7-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="aa5f7-144">상속자</span><span class="sxs-lookup"><span data-stu-id="aa5f7-144">NOTES</span></span>

## <span data-ttu-id="aa5f7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa5f7-145">RELATED LINKS</span></span>

[<span data-ttu-id="aa5f7-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa5f7-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="aa5f7-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa5f7-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
