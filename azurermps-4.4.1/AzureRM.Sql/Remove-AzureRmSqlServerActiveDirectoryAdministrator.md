---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 030a5ed61b4faafb47e8cba808dada484180a01c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711762"
---
# <span data-ttu-id="d7ca9-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7ca9-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="d7ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ca9-103">SQL Server에 대 한 Azure AD 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ca9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7ca9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7ca9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ca9-106">**AzureRmSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Server에 대 한 azure AD (Active Directory) 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="d7ca9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="d7ca9-108">예제 1: 관리자 제거</span><span class="sxs-lookup"><span data-stu-id="d7ca9-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="d7ca9-109">이 명령은 리소스 그룹 ResourceGroup01와 연결 된 Server01 서버에 대 한 Azure AD 관리자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d7ca9-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7ca9-110">PARAMETERS</span></span>

### <span data-ttu-id="d7ca9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d7ca9-111">-Force</span></span>
<span data-ttu-id="d7ca9-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7ca9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ca9-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7ca9-114">SQL Server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="d7ca9-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7ca9-115">-ServerName</span></span>
<span data-ttu-id="d7ca9-116">이 cmdlet이 관리자를 제거 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-116">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="d7ca9-117">-확인</span><span class="sxs-lookup"><span data-stu-id="d7ca9-117">-Confirm</span></span>
<span data-ttu-id="d7ca9-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ca9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ca9-119">-WhatIf</span></span>
<span data-ttu-id="d7ca9-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ca9-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ca9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ca9-122">-DefaultProfile</span></span>
<span data-ttu-id="d7ca9-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ca9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ca9-124">CommonParameters</span></span>
<span data-ttu-id="d7ca9-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ca9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ca9-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ca9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ca9-127">입력</span><span class="sxs-lookup"><span data-stu-id="d7ca9-127">INPUTS</span></span>

### <span data-ttu-id="d7ca9-128">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d7ca9-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="d7ca9-129">출력</span><span class="sxs-lookup"><span data-stu-id="d7ca9-129">OUTPUTS</span></span>

### <span data-ttu-id="d7ca9-130">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d7ca9-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="d7ca9-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d7ca9-131">NOTES</span></span>

## <span data-ttu-id="d7ca9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7ca9-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7ca9-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7ca9-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d7ca9-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7ca9-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d7ca9-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d7ca9-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


