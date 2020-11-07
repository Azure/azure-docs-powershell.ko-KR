---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 8a034bc85209e0325547bac2f64f277ceaee0abc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873800"
---
# <span data-ttu-id="4b6d0-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4b6d0-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="4b6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6d0-103">SQL 관리 인스턴스에 대 한 Azure AD 관리자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="4b6d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b6d0-104">SYNTAX</span></span>

### <span data-ttu-id="4b6d0-105">UseResourceGroupAndInstanceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b6d0-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b6d0-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b6d0-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b6d0-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b6d0-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b6d0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4b6d0-108">DESCRIPTION</span></span>
<span data-ttu-id="4b6d0-109">**AzSqlInstanceActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL 관리 되는 인스턴스의 azure AD (Active Directory) 관리자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="4b6d0-110">한 번에 하나의 관리자만 프로 비전 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="4b6d0-111">Azure AD의 다음 구성원을 SQL 관리 인스턴스 관리자로 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="4b6d0-112">Azure AD의 네이티브 구성원</span><span class="sxs-lookup"><span data-stu-id="4b6d0-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="4b6d0-113">Azure AD의 페더레이션 구성원</span><span class="sxs-lookup"><span data-stu-id="4b6d0-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="4b6d0-114">보안 그룹으로 만든 azure AD 그룹 다른 Azure 광고의 구성원은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="4b6d0-115">Microsoft 계정 (예: Outlook.com, Hotmail.com 또는 Live.com domains)은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="4b6d0-116">Gmail.com 또는 Yahoo.com 도메인에 있는 것과 같은 다른 게스트 계정은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="4b6d0-117">전용 Azure AD 그룹을 관리자로 프로 비전 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="4b6d0-118">예제의</span><span class="sxs-lookup"><span data-stu-id="4b6d0-118">EXAMPLES</span></span>

### <span data-ttu-id="4b6d0-119">예제 1: 리소스 그룹과 연결 된 관리 되는 인스턴스에 대 한 관리자 그룹 프로 비전</span><span class="sxs-lookup"><span data-stu-id="4b6d0-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="4b6d0-120">이 명령은 ManagedInstance01 이라는 관리 되는 인스턴스에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="4b6d0-121">이 서버는 리소스 그룹 ResourceGroup01 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="4b6d0-122">예제 2: 관리 되는 인스턴스 개체를 사용 하 여 관리자 사용자 프로 비전</span><span class="sxs-lookup"><span data-stu-id="4b6d0-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="4b6d0-123">이 명령은 관리 되는 인스턴스 개체에서 Azure AD 사용자를 관리자로 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="4b6d0-124">예제 3: 관리 되는 인스턴스 리소스 식별자를 사용 하 여 관리자 프로 비전</span><span class="sxs-lookup"><span data-stu-id="4b6d0-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="4b6d0-125">이 명령은 관리 되는 인스턴스 리소스 식별자를 사용 하 여 Azure AD 사용자를 관리자로 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="4b6d0-126">변수</span><span class="sxs-lookup"><span data-stu-id="4b6d0-126">PARAMETERS</span></span>

### <span data-ttu-id="4b6d0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6d0-127">-DefaultProfile</span></span>
<span data-ttu-id="4b6d0-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b6d0-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4b6d0-129">-DisplayName</span></span>
<span data-ttu-id="4b6d0-130">권한을 부여할 사용자 또는 그룹의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="4b6d0-131">이 표시 이름은 현재 구독과 연결 된 active directory에 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="4b6d0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b6d0-132">-InputObject</span></span>
<span data-ttu-id="4b6d0-133">사용할 관리 되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6d0-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4b6d0-134">-InstanceName</span></span>
<span data-ttu-id="4b6d0-135">SQL 관리 되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="4b6d0-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4b6d0-136">-ObjectId</span></span>
<span data-ttu-id="4b6d0-137">사용 권한을 부여할 Azure Active Directory의 사용자 또는 그룹의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="4b6d0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b6d0-138">-ResourceGroupName</span></span>
<span data-ttu-id="4b6d0-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b6d0-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b6d0-140">-ResourceId</span></span>
<span data-ttu-id="4b6d0-141">사용할 인스턴스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="4b6d0-142">-확인</span><span class="sxs-lookup"><span data-stu-id="4b6d0-142">-Confirm</span></span>
<span data-ttu-id="4b6d0-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b6d0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6d0-144">-WhatIf</span></span>
<span data-ttu-id="4b6d0-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b6d0-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b6d0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6d0-147">CommonParameters</span></span>
<span data-ttu-id="4b6d0-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6d0-149">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b6d0-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6d0-150">입력</span><span class="sxs-lookup"><span data-stu-id="4b6d0-150">INPUTS</span></span>

### <span data-ttu-id="4b6d0-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4b6d0-151">System.String</span></span>

### <span data-ttu-id="4b6d0-152">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="4b6d0-152">System.Guid</span></span>

## <span data-ttu-id="4b6d0-153">출력</span><span class="sxs-lookup"><span data-stu-id="4b6d0-153">OUTPUTS</span></span>

### <span data-ttu-id="4b6d0-154">InstanceActiveDirectoryAdministrator. AzureSqlInstanceActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="4b6d0-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="4b6d0-155">상속자</span><span class="sxs-lookup"><span data-stu-id="4b6d0-155">NOTES</span></span>

## <span data-ttu-id="4b6d0-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b6d0-156">RELATED LINKS</span></span>

[<span data-ttu-id="4b6d0-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4b6d0-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="4b6d0-158">제거-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4b6d0-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
