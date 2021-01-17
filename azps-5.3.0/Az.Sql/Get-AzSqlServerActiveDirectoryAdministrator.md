---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492323"
---
# <span data-ttu-id="3b77b-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3b77b-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="3b77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b77b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b77b-103">Azure AD 관리자에 대한 정보를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b77b-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="3b77b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3b77b-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b77b-105">설명</span><span class="sxs-lookup"><span data-stu-id="3b77b-105">DESCRIPTION</span></span>
<span data-ttu-id="3b77b-106">**Get-AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL 서버에 대한 Azure AD(Azure Active Directory) 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="3b77b-107">예제</span><span class="sxs-lookup"><span data-stu-id="3b77b-107">EXAMPLES</span></span>

### <span data-ttu-id="3b77b-108">예제 1: 서버의 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="3b77b-109">이 명령은 ResourceGroup01이라는 리소스 그룹과 연결된 Server01 서버의 Azure AD 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3b77b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b77b-110">PARAMETERS</span></span>

### <span data-ttu-id="3b77b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b77b-111">-DefaultProfile</span></span>
<span data-ttu-id="3b77b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3b77b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b77b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b77b-113">-ResourceGroupName</span></span>
<span data-ttu-id="3b77b-114">리소스 그룹이 할당된 리소스 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="3b77b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b77b-115">-ServerName</span></span>
<span data-ttu-id="3b77b-116">이 cmdlet이 정보를 SQL Server 이름의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="3b77b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b77b-117">-Confirm</span></span>
<span data-ttu-id="3b77b-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b77b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b77b-119">-WhatIf</span></span>
<span data-ttu-id="3b77b-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3b77b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b77b-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b77b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b77b-122">CommonParameters</span></span>
<span data-ttu-id="3b77b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3b77b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b77b-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b77b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b77b-125">입력</span><span class="sxs-lookup"><span data-stu-id="3b77b-125">INPUTS</span></span>

### <span data-ttu-id="3b77b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3b77b-126">System.String</span></span>

## <span data-ttu-id="3b77b-127">출력</span><span class="sxs-lookup"><span data-stu-id="3b77b-127">OUTPUTS</span></span>

### <span data-ttu-id="3b77b-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="3b77b-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="3b77b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3b77b-129">NOTES</span></span>

## <span data-ttu-id="3b77b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b77b-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b77b-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3b77b-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3b77b-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3b77b-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3b77b-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3b77b-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3b77b-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="3b77b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


