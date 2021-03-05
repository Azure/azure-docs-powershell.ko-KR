---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 37fe534b13226f81c7639275a3c35f3a54d3543b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981536"
---
# <span data-ttu-id="a5d04-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a5d04-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a5d04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d04-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d04-103">Azure AD 관리자를 프로비전하여 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5d04-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a5d04-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5d04-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d04-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5d04-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d04-106">**Set-AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Server에 대한 Azure AD(Azure Active Directory) 관리자를 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="a5d04-107">한 번씩 하나의 관리자만 프로비전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="a5d04-108">Azure AD의 다음 구성원을 관리자 권한으로 프로비전할 SQL Server 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="a5d04-109">Azure AD의 네이티브 멤버</span><span class="sxs-lookup"><span data-stu-id="a5d04-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="a5d04-110">Azure AD의 페더리드 멤버</span><span class="sxs-lookup"><span data-stu-id="a5d04-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="a5d04-111">네이티브 또는 페더리드 멤버인 다른 Azure AD에서 가져온 멤버</span><span class="sxs-lookup"><span data-stu-id="a5d04-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="a5d04-112">보안 그룹으로 만든 Azure AD 그룹(예: Outlook.com, Hotmail.com 또는 Live.com 도메인의 경우)은 관리자 권한으로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a5d04-113">다른 게스트 계정(예: Gmail.com 또는 Yahoo.com)은 관리자 권한으로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a5d04-114">관리자 권한으로 전용 Azure AD 그룹을 프로비전하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="a5d04-115">예제</span><span class="sxs-lookup"><span data-stu-id="a5d04-115">EXAMPLES</span></span>

### <span data-ttu-id="a5d04-116">예제 1: 서버에 대한 관리자 그룹 프로비전</span><span class="sxs-lookup"><span data-stu-id="a5d04-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="a5d04-117">이 명령은 Server01이라는 서버에 대해 DBAs라는 Azure AD 관리자 그룹을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a5d04-118">이 서버는 리소스 그룹 ResourceGroup01과 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a5d04-119">예제 2: 서버에 대한 관리자 사용자 프로비전</span><span class="sxs-lookup"><span data-stu-id="a5d04-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="a5d04-120">이 명령은 Server01이라는 서버에 대한 관리자로 Azure AD 사용자를 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="a5d04-121">예제 3: ID를 지정하여 관리자 그룹 프로비전</span><span class="sxs-lookup"><span data-stu-id="a5d04-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="a5d04-122">이 명령은 Server01이라는 서버에 대해 DBAs라는 Azure AD 관리자 그룹을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a5d04-123">명령은 ObjectId 매개 변수에 대한 *ID를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="a5d04-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="a5d04-124">이렇게 하면 그룹의 표시 이름이 고유하지 않은 경우에도 명령이 성공합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="a5d04-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5d04-125">PARAMETERS</span></span>

### <span data-ttu-id="a5d04-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d04-126">-DefaultProfile</span></span>
<span data-ttu-id="a5d04-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a5d04-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5d04-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a5d04-128">-DisplayName</span></span>
<span data-ttu-id="a5d04-129">이 cmdlet이 프로비전하는 Azure AD 관리자의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="a5d04-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a5d04-130">-ObjectId</span></span>
<span data-ttu-id="a5d04-131">이 cmdlet이 프로비전하는 Azure AD 관리자의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="a5d04-132">표시 이름이 고유하지 않은 경우 이 매개 변수에 대한 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d04-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d04-133">-ResourceGroupName</span></span>
<span data-ttu-id="a5d04-134">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a5d04-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5d04-135">-ServerName</span></span>
<span data-ttu-id="a5d04-136">이 cmdlet이 관리자를 프로비전하는 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d04-137">-확인</span><span class="sxs-lookup"><span data-stu-id="a5d04-137">-Confirm</span></span>
<span data-ttu-id="a5d04-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d04-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d04-139">-WhatIf</span></span>
<span data-ttu-id="a5d04-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d04-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d04-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d04-142">CommonParameters</span></span>
<span data-ttu-id="a5d04-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d04-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d04-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d04-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d04-145">입력</span><span class="sxs-lookup"><span data-stu-id="a5d04-145">INPUTS</span></span>

### <span data-ttu-id="a5d04-146">System.String</span><span class="sxs-lookup"><span data-stu-id="a5d04-146">System.String</span></span>

### <span data-ttu-id="a5d04-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a5d04-147">System.Guid</span></span>

## <span data-ttu-id="a5d04-148">출력</span><span class="sxs-lookup"><span data-stu-id="a5d04-148">OUTPUTS</span></span>

### <span data-ttu-id="a5d04-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a5d04-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a5d04-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5d04-150">NOTES</span></span>

## <span data-ttu-id="a5d04-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5d04-151">RELATED LINKS</span></span>

[<span data-ttu-id="a5d04-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a5d04-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a5d04-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a5d04-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a5d04-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a5d04-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a5d04-155">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a5d04-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


