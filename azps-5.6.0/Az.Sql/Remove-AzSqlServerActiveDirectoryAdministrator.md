---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: ac6b421a64658423857c93ff0c782b0ec84b8c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995190"
---
# <span data-ttu-id="72568-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="72568-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="72568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72568-102">SYNOPSIS</span></span>
<span data-ttu-id="72568-103">Azure AD 관리자를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="72568-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="72568-104">구문</span><span class="sxs-lookup"><span data-stu-id="72568-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72568-105">설명</span><span class="sxs-lookup"><span data-stu-id="72568-105">DESCRIPTION</span></span>
<span data-ttu-id="72568-106">**Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Server에 대한 Azure AD(Azure Active Directory) 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="72568-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="72568-107">예제</span><span class="sxs-lookup"><span data-stu-id="72568-107">EXAMPLES</span></span>

### <span data-ttu-id="72568-108">예제 1: 관리자 제거</span><span class="sxs-lookup"><span data-stu-id="72568-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="72568-109">이 명령은 리소스 그룹 ResourceGroup01과 연결된 Server01이라는 서버에 대한 Azure AD 관리자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="72568-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="72568-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="72568-110">PARAMETERS</span></span>

### <span data-ttu-id="72568-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72568-111">-DefaultProfile</span></span>
<span data-ttu-id="72568-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="72568-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72568-113">-Force</span><span class="sxs-lookup"><span data-stu-id="72568-113">-Force</span></span>
<span data-ttu-id="72568-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="72568-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72568-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72568-115">-ResourceGroupName</span></span>
<span data-ttu-id="72568-116">리소스가 할당된 리소스 그룹의 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="72568-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="72568-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72568-117">-ServerName</span></span>
<span data-ttu-id="72568-118">이 cmdlet이 관리자를 제거하는 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="72568-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="72568-119">-확인</span><span class="sxs-lookup"><span data-stu-id="72568-119">-Confirm</span></span>
<span data-ttu-id="72568-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="72568-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72568-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72568-121">-WhatIf</span></span>
<span data-ttu-id="72568-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="72568-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72568-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72568-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72568-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72568-124">CommonParameters</span></span>
<span data-ttu-id="72568-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="72568-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72568-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72568-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72568-127">입력</span><span class="sxs-lookup"><span data-stu-id="72568-127">INPUTS</span></span>

### <span data-ttu-id="72568-128">System.String</span><span class="sxs-lookup"><span data-stu-id="72568-128">System.String</span></span>

## <span data-ttu-id="72568-129">출력</span><span class="sxs-lookup"><span data-stu-id="72568-129">OUTPUTS</span></span>

### <span data-ttu-id="72568-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="72568-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="72568-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="72568-131">NOTES</span></span>

## <span data-ttu-id="72568-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72568-132">RELATED LINKS</span></span>

[<span data-ttu-id="72568-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="72568-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="72568-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="72568-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="72568-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="72568-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


