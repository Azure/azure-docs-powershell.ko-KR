---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042017"
---
# <span data-ttu-id="b7b14-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b7b14-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="b7b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7b14-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b14-103">특정 SQL Server에 대해 Azure AD 전용 인증을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="b7b14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7b14-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b14-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b7b14-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b14-106">**AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet은 현재 구독의 AzureSQL 서버에 대 한 azure AD (Active Directory) 인증 요구 사항만 사용할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="b7b14-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b7b14-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b14-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7b14-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="b7b14-109">이 명령은 ResourceGroup01 이라는 리소스 그룹과 연결 된 Server01 이라는 AzureSQL server에 대해 azure AD (Active Directory)만 인증 요구 사항을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b7b14-110">변수</span><span class="sxs-lookup"><span data-stu-id="b7b14-110">PARAMETERS</span></span>

### <span data-ttu-id="b7b14-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b14-111">-DefaultProfile</span></span>
<span data-ttu-id="b7b14-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b14-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b14-113">-ResourceGroupName</span></span>
<span data-ttu-id="b7b14-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7b14-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7b14-115">-ServerName</span></span>
<span data-ttu-id="b7b14-116">Azure Active Directory 관리자가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

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

### <span data-ttu-id="b7b14-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b7b14-117">-Confirm</span></span>
<span data-ttu-id="b7b14-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b14-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b14-119">-WhatIf</span></span>
<span data-ttu-id="b7b14-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b14-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b14-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b14-122">CommonParameters</span></span>
<span data-ttu-id="b7b14-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b14-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b14-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7b14-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b14-125">입력</span><span class="sxs-lookup"><span data-stu-id="b7b14-125">INPUTS</span></span>

### <span data-ttu-id="b7b14-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b7b14-126">System.String</span></span>

## <span data-ttu-id="b7b14-127">출력</span><span class="sxs-lookup"><span data-stu-id="b7b14-127">OUTPUTS</span></span>

### <span data-ttu-id="b7b14-128">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryAdministratorModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="b7b14-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b7b14-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b7b14-129">NOTES</span></span>

## <span data-ttu-id="b7b14-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7b14-130">RELATED LINKS</span></span>

[<span data-ttu-id="b7b14-131">제거-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7b14-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7b14-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7b14-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7b14-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7b14-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7b14-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b7b14-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
