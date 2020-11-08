---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f3492b0f6eb83f2c4a37a6fa073e7f579208cf62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204820"
---
# <span data-ttu-id="28c3a-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="28c3a-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="28c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="28c3a-103">SQL Server에 대 한 Azure AD 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="28c3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28c3a-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="28c3a-106">**AzSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독의 AzureSQL 서버에 대 한 azure AD (Azure Active Directory) 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="28c3a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="28c3a-108">예제 1: 서버의 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="28c3a-109">이 명령은 ResourceGroup01 이라는 리소스 그룹과 연결 된 Server01 이라는 서버의 Azure AD 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="28c3a-110">변수</span><span class="sxs-lookup"><span data-stu-id="28c3a-110">PARAMETERS</span></span>

### <span data-ttu-id="28c3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c3a-111">-DefaultProfile</span></span>
<span data-ttu-id="28c3a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="28c3a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28c3a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c3a-113">-ResourceGroupName</span></span>
<span data-ttu-id="28c3a-114">SQL Server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="28c3a-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28c3a-115">-ServerName</span></span>
<span data-ttu-id="28c3a-116">이 cmdlet에서 정보를 가져오는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="28c3a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="28c3a-117">-Confirm</span></span>
<span data-ttu-id="28c3a-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c3a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c3a-119">-WhatIf</span></span>
<span data-ttu-id="28c3a-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c3a-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c3a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c3a-122">CommonParameters</span></span>
<span data-ttu-id="28c3a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28c3a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c3a-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28c3a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c3a-125">입력</span><span class="sxs-lookup"><span data-stu-id="28c3a-125">INPUTS</span></span>

### <span data-ttu-id="28c3a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28c3a-126">System.String</span></span>

## <span data-ttu-id="28c3a-127">출력</span><span class="sxs-lookup"><span data-stu-id="28c3a-127">OUTPUTS</span></span>

### <span data-ttu-id="28c3a-128">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="28c3a-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="28c3a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="28c3a-129">NOTES</span></span>

## <span data-ttu-id="28c3a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28c3a-130">RELATED LINKS</span></span>

[<span data-ttu-id="28c3a-131">제거-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="28c3a-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="28c3a-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="28c3a-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="28c3a-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="28c3a-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="28c3a-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="28c3a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


