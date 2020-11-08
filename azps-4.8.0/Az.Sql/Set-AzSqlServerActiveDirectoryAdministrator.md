---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213865"
---
# <span data-ttu-id="f199f-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f199f-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f199f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f199f-102">SYNOPSIS</span></span>
<span data-ttu-id="f199f-103">SQL Server 용 Azure AD 관리자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="f199f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f199f-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f199f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f199f-105">DESCRIPTION</span></span>
<span data-ttu-id="f199f-106">**AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독의 AzureSQL Server에 대 한 azure AD (Azure Active Directory) 관리자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="f199f-107">한 번에 하나의 관리자만 프로 비전 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="f199f-108">Azure AD의 다음 구성원을 SQL Server 관리자로 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="f199f-109">Azure AD의 네이티브 구성원</span><span class="sxs-lookup"><span data-stu-id="f199f-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="f199f-110">Azure AD의 페더레이션 구성원</span><span class="sxs-lookup"><span data-stu-id="f199f-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="f199f-111">기본 또는 페더레이션 구성원 인 다른 Azure 광고에서 가져온 구성원</span><span class="sxs-lookup"><span data-stu-id="f199f-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="f199f-112">Microsoft 계정 (예: Outlook.com, Hotmail.com 또는 Live.com domains)으로 만든 Azure AD 그룹은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f199f-113">Gmail.com 또는 Yahoo.com 도메인에 있는 것과 같은 다른 게스트 계정은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f199f-114">전용 Azure AD 그룹을 관리자로 프로 비전 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="f199f-115">예제의</span><span class="sxs-lookup"><span data-stu-id="f199f-115">EXAMPLES</span></span>

### <span data-ttu-id="f199f-116">예제 1: 서버에 대 한 관리자 그룹 프로 비전</span><span class="sxs-lookup"><span data-stu-id="f199f-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="f199f-117">이 명령은 Server01 이라는 서버에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="f199f-118">이 서버는 리소스 그룹 ResourceGroup01 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f199f-119">예제 2: 서버에 대 한 관리자 사용자 프로 비전</span><span class="sxs-lookup"><span data-stu-id="f199f-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="f199f-120">이 명령은 Server01 이라는 서버의 관리자로 Azure AD 사용자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="f199f-121">예제 3: ID를 지정 하 여 관리자 그룹 프로 비전</span><span class="sxs-lookup"><span data-stu-id="f199f-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="f199f-122">이 명령은 Server01 이라는 서버에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="f199f-123">Command는 *ObjectId* 매개 변수에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="f199f-124">이렇게 하면 그룹의 표시 이름이 고유 하지 않은 경우에도 명령이 성공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="f199f-125">변수</span><span class="sxs-lookup"><span data-stu-id="f199f-125">PARAMETERS</span></span>

### <span data-ttu-id="f199f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f199f-126">-DefaultProfile</span></span>
<span data-ttu-id="f199f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f199f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f199f-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f199f-128">-DisplayName</span></span>
<span data-ttu-id="f199f-129">이 cmdlet이 프로 비전 하는 Azure AD 관리자의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="f199f-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f199f-130">-ObjectId</span></span>
<span data-ttu-id="f199f-131">이 cmdlet이 프로 비전 하는 Azure AD 관리자의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="f199f-132">표시 이름이 고유 하지 않은 경우이 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="f199f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f199f-133">-ResourceGroupName</span></span>
<span data-ttu-id="f199f-134">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f199f-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f199f-135">-ServerName</span></span>
<span data-ttu-id="f199f-136">이 cmdlet이 관리자를 프로 비전 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="f199f-137">-확인</span><span class="sxs-lookup"><span data-stu-id="f199f-137">-Confirm</span></span>
<span data-ttu-id="f199f-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f199f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f199f-139">-WhatIf</span></span>
<span data-ttu-id="f199f-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f199f-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f199f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f199f-142">CommonParameters</span></span>
<span data-ttu-id="f199f-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f199f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f199f-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f199f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f199f-145">입력</span><span class="sxs-lookup"><span data-stu-id="f199f-145">INPUTS</span></span>

### <span data-ttu-id="f199f-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f199f-146">System.String</span></span>

### <span data-ttu-id="f199f-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="f199f-147">System.Guid</span></span>

## <span data-ttu-id="f199f-148">출력</span><span class="sxs-lookup"><span data-stu-id="f199f-148">OUTPUTS</span></span>

### <span data-ttu-id="f199f-149">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="f199f-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="f199f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f199f-150">NOTES</span></span>

## <span data-ttu-id="f199f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f199f-151">RELATED LINKS</span></span>

[<span data-ttu-id="f199f-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f199f-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f199f-153">제거-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f199f-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f199f-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f199f-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f199f-155">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f199f-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


