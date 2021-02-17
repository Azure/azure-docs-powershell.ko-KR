---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198505"
---
# <span data-ttu-id="67871-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="67871-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="67871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67871-102">SYNOPSIS</span></span>
<span data-ttu-id="67871-103">사용자에 대한 Azure AD 관리자를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="67871-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="67871-104">구문</span><span class="sxs-lookup"><span data-stu-id="67871-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67871-105">설명</span><span class="sxs-lookup"><span data-stu-id="67871-105">DESCRIPTION</span></span>
<span data-ttu-id="67871-106">**Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Server에 대한 Azure AD(Azure Active Directory) 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67871-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="67871-107">예제</span><span class="sxs-lookup"><span data-stu-id="67871-107">EXAMPLES</span></span>

### <span data-ttu-id="67871-108">예제 1: 관리자 제거</span><span class="sxs-lookup"><span data-stu-id="67871-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="67871-109">이 명령은 리소스 그룹 ResourceGroup01과 연결된 Server01 서버에 대한 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67871-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="67871-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67871-110">PARAMETERS</span></span>

### <span data-ttu-id="67871-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67871-111">-DefaultProfile</span></span>
<span data-ttu-id="67871-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67871-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67871-113">-Force</span><span class="sxs-lookup"><span data-stu-id="67871-113">-Force</span></span>
<span data-ttu-id="67871-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="67871-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67871-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67871-115">-ResourceGroupName</span></span>
<span data-ttu-id="67871-116">리소스 그룹이 할당된 리소스 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67871-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="67871-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67871-117">-ServerName</span></span>
<span data-ttu-id="67871-118">이 cmdlet이 관리자를 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67871-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="67871-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67871-119">-Confirm</span></span>
<span data-ttu-id="67871-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67871-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67871-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67871-121">-WhatIf</span></span>
<span data-ttu-id="67871-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="67871-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67871-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67871-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67871-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67871-124">CommonParameters</span></span>
<span data-ttu-id="67871-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67871-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67871-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67871-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67871-127">입력</span><span class="sxs-lookup"><span data-stu-id="67871-127">INPUTS</span></span>

### <span data-ttu-id="67871-128">System.String</span><span class="sxs-lookup"><span data-stu-id="67871-128">System.String</span></span>

## <span data-ttu-id="67871-129">출력</span><span class="sxs-lookup"><span data-stu-id="67871-129">OUTPUTS</span></span>

### <span data-ttu-id="67871-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="67871-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="67871-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67871-131">NOTES</span></span>

## <span data-ttu-id="67871-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67871-132">RELATED LINKS</span></span>

[<span data-ttu-id="67871-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="67871-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="67871-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="67871-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="67871-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="67871-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


