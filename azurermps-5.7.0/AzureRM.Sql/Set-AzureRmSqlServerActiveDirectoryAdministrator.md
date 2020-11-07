---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 43dbbe6ca4f24e98bcfc45703c387ccb5fb4db03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702508"
---
# <span data-ttu-id="f614f-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f614f-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f614f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f614f-102">SYNOPSIS</span></span>
<span data-ttu-id="f614f-103">SQL Server 용 Azure AD 관리자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f614f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f614f-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f614f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f614f-105">DESCRIPTION</span></span>
<span data-ttu-id="f614f-106">**AzureRmSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독의 AzureSQL Server에 대 한 azure AD (Azure Active Directory) 관리자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="f614f-107">한 번에 하나의 관리자만 프로 비전 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="f614f-108">Azure AD의 다음 구성원을 SQL Server 관리자로 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="f614f-109">Azure AD의 네이티브 구성원</span><span class="sxs-lookup"><span data-stu-id="f614f-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="f614f-110">Azure AD의 페더레이션 구성원</span><span class="sxs-lookup"><span data-stu-id="f614f-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="f614f-111">기본 또는 페더레이션 구성원 인 다른 Azure 광고에서 가져온 구성원</span><span class="sxs-lookup"><span data-stu-id="f614f-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="f614f-112">Azure AD 그룹을 보안 그룹으로 만듦</span><span class="sxs-lookup"><span data-stu-id="f614f-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="f614f-113">Microsoft 계정 (예: Outlook.com, Hotmail.com 또는 Live.com domains)은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f614f-114">Gmail.com 또는 Yahoo.com 도메인에 있는 것과 같은 다른 게스트 계정은 관리자로 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="f614f-115">전용 Azure AD 그룹을 관리자로 프로 비전 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="f614f-116">예제의</span><span class="sxs-lookup"><span data-stu-id="f614f-116">EXAMPLES</span></span>

### <span data-ttu-id="f614f-117">예제 1: 서버에 대 한 관리자 그룹 프로 비전</span><span class="sxs-lookup"><span data-stu-id="f614f-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="f614f-118">이 명령은 Server01 이라는 서버에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="f614f-119">이 서버는 리소스 그룹 ResourceGroup01 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f614f-120">예제 2: 서버에 대 한 관리자 사용자 프로 비전</span><span class="sxs-lookup"><span data-stu-id="f614f-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="f614f-121">이 명령은 Server01 이라는 서버의 관리자로 Azure AD 사용자를 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="f614f-122">예제 3: ID를 지정 하 여 관리자 그룹 프로 비전</span><span class="sxs-lookup"><span data-stu-id="f614f-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="f614f-123">이 명령은 Server01 이라는 서버에 대 한 Dba 라는 Azure AD 관리자 그룹을 프로 비전 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="f614f-124">Command는 *ObjectId* 매개 변수에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="f614f-125">이렇게 하면 그룹의 표시 이름이 고유 하지 않은 경우에도 명령이 성공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="f614f-126">변수</span><span class="sxs-lookup"><span data-stu-id="f614f-126">PARAMETERS</span></span>

### <span data-ttu-id="f614f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f614f-127">-DefaultProfile</span></span>
<span data-ttu-id="f614f-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f614f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f614f-129">-DisplayName</span></span>
<span data-ttu-id="f614f-130">이 cmdlet이 프로 비전 하는 Azure AD 관리자의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-130">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f614f-131">-ObjectId</span></span>
<span data-ttu-id="f614f-132">이 cmdlet이 프로 비전 하는 Azure AD 관리자의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-132">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="f614f-133">표시 이름이 고유 하지 않은 경우이 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-133">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f614f-134">-ResourceGroupName</span></span>
<span data-ttu-id="f614f-135">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-135">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f614f-136">-ServerName</span></span>
<span data-ttu-id="f614f-137">이 cmdlet이 관리자를 프로 비전 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-137">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="f614f-138">-Confirm</span></span>
<span data-ttu-id="f614f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f614f-140">-WhatIf</span></span>
<span data-ttu-id="f614f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f614f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f614f-143">CommonParameters</span></span>
<span data-ttu-id="f614f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f614f-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f614f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f614f-146">입력</span><span class="sxs-lookup"><span data-stu-id="f614f-146">INPUTS</span></span>

### <span data-ttu-id="f614f-147">않아야</span><span class="sxs-lookup"><span data-stu-id="f614f-147">None</span></span>
<span data-ttu-id="f614f-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f614f-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f614f-149">출력</span><span class="sxs-lookup"><span data-stu-id="f614f-149">OUTPUTS</span></span>

### <span data-ttu-id="f614f-150">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="f614f-150">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="f614f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f614f-151">NOTES</span></span>

## <span data-ttu-id="f614f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f614f-152">RELATED LINKS</span></span>

[<span data-ttu-id="f614f-153">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f614f-153">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f614f-154">제거-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f614f-154">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f614f-155">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f614f-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


