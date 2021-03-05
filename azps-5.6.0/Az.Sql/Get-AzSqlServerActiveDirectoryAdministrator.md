---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 09b7ebf1f88479bca847566b2da93feb83b18571
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974219"
---
# <span data-ttu-id="5e0d4-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5e0d4-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="5e0d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0d4-103">Azure AD 관리자에 대한 정보를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="5e0d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e0d4-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="5e0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0d4-106">**Get-AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Server에 대한 Azure AD(Azure Active Directory) 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="5e0d4-107">예제</span><span class="sxs-lookup"><span data-stu-id="5e0d4-107">EXAMPLES</span></span>

### <span data-ttu-id="5e0d4-108">예제 1: 서버에 대한 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="5e0d4-109">이 명령은 ResourceGroup01이라는 리소스 그룹과 연결된 Server01이라는 서버에 대한 Azure AD 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="5e0d4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5e0d4-110">PARAMETERS</span></span>

### <span data-ttu-id="5e0d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0d4-111">-DefaultProfile</span></span>
<span data-ttu-id="5e0d4-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5e0d4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e0d4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0d4-113">-ResourceGroupName</span></span>
<span data-ttu-id="5e0d4-114">리소스가 할당된 리소스 그룹의 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5e0d4-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e0d4-115">-ServerName</span></span>
<span data-ttu-id="5e0d4-116">이 cmdlet에서 정보를 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="5e0d4-117">-확인</span><span class="sxs-lookup"><span data-stu-id="5e0d4-117">-Confirm</span></span>
<span data-ttu-id="5e0d4-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0d4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0d4-119">-WhatIf</span></span>
<span data-ttu-id="5e0d4-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0d4-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0d4-122">CommonParameters</span></span>
<span data-ttu-id="5e0d4-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e0d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0d4-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e0d4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0d4-125">입력</span><span class="sxs-lookup"><span data-stu-id="5e0d4-125">INPUTS</span></span>

### <span data-ttu-id="5e0d4-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5e0d4-126">System.String</span></span>

## <span data-ttu-id="5e0d4-127">출력</span><span class="sxs-lookup"><span data-stu-id="5e0d4-127">OUTPUTS</span></span>

### <span data-ttu-id="5e0d4-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="5e0d4-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="5e0d4-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e0d4-129">NOTES</span></span>

## <span data-ttu-id="5e0d4-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e0d4-130">RELATED LINKS</span></span>

[<span data-ttu-id="5e0d4-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5e0d4-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5e0d4-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5e0d4-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5e0d4-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="5e0d4-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="5e0d4-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5e0d4-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


