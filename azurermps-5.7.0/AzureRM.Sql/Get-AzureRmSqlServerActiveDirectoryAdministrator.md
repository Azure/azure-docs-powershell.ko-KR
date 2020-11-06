---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: e782ef221474ab3a041fddc7628157fd999796d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528787"
---
# <span data-ttu-id="b7522-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7522-101">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b7522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7522-102">SYNOPSIS</span></span>
<span data-ttu-id="b7522-103">SQL Server에 대 한 Azure AD 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7522-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7522-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7522-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b7522-105">DESCRIPTION</span></span>
<span data-ttu-id="b7522-106">**AzureRmSqlServerActiveDirectoryAdministrator** cmdlet은 현재 구독의 AzureSQL 서버에 대 한 azure AD (Azure Active Directory) 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-106">The **Get-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="b7522-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b7522-107">EXAMPLES</span></span>

### <span data-ttu-id="b7522-108">예제 1: 서버의 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b7522-109">이 명령은 ResourceGroup01 이라는 리소스 그룹과 연결 된 Server01 이라는 서버의 Azure AD 관리자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b7522-110">변수</span><span class="sxs-lookup"><span data-stu-id="b7522-110">PARAMETERS</span></span>

### <span data-ttu-id="b7522-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7522-111">-DefaultProfile</span></span>
<span data-ttu-id="b7522-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b7522-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7522-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7522-113">-ResourceGroupName</span></span>
<span data-ttu-id="b7522-114">SQL Server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="b7522-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7522-115">-ServerName</span></span>
<span data-ttu-id="b7522-116">이 cmdlet에서 정보를 가져오는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="b7522-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b7522-117">-Confirm</span></span>
<span data-ttu-id="b7522-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7522-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7522-119">-WhatIf</span></span>
<span data-ttu-id="b7522-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7522-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7522-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7522-122">CommonParameters</span></span>
<span data-ttu-id="b7522-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7522-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7522-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7522-125">입력</span><span class="sxs-lookup"><span data-stu-id="b7522-125">INPUTS</span></span>

### <span data-ttu-id="b7522-126">않아야</span><span class="sxs-lookup"><span data-stu-id="b7522-126">None</span></span>
<span data-ttu-id="b7522-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7522-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7522-128">출력</span><span class="sxs-lookup"><span data-stu-id="b7522-128">OUTPUTS</span></span>

### <span data-ttu-id="b7522-129">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="b7522-129">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b7522-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b7522-130">NOTES</span></span>

## <span data-ttu-id="b7522-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7522-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7522-132">제거-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7522-132">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7522-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7522-133">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7522-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b7522-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


