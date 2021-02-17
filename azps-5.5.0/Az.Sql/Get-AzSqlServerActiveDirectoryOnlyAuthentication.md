---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191057"
---
# <span data-ttu-id="5ad64-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="5ad64-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="5ad64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad64-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad64-103">특정 리소스에 대한 Azure AD 전용 인증을 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ad64-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="5ad64-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ad64-104">SYNTAX</span></span>

### <span data-ttu-id="5ad64-105">UseResourceGroupAndServerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5ad64-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad64-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ad64-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad64-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ad64-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad64-108">설명</span><span class="sxs-lookup"><span data-stu-id="5ad64-108">DESCRIPTION</span></span>
<span data-ttu-id="5ad64-109">**Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet은 현재 구독에서 AzureSQL 서버에 대한 Azure AD(Azure Active Directory) 인증 요구 사항만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="5ad64-110">예제</span><span class="sxs-lookup"><span data-stu-id="5ad64-110">EXAMPLES</span></span>

### <span data-ttu-id="5ad64-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ad64-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="5ad64-112">이 명령은 ResourceGroup01이라는 리소스 그룹과 연결된 Server01이라는 AzureSQL 서버에 대한 Azure AD(Azure Active Directory) 인증 요구 사항만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="5ad64-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ad64-113">PARAMETERS</span></span>

### <span data-ttu-id="5ad64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad64-114">-DefaultProfile</span></span>
<span data-ttu-id="5ad64-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ad64-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ad64-116">-InputObject</span></span>
<span data-ttu-id="5ad64-117">사용할 SQL 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad64-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad64-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ad64-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad64-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ad64-120">-ResourceId</span></span>
<span data-ttu-id="5ad64-121">사용할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5ad64-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad64-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ad64-122">-ServerName</span></span>
<span data-ttu-id="5ad64-123">Azure Active Directory SQL Server 있는 Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad64-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ad64-124">-Confirm</span></span>
<span data-ttu-id="5ad64-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad64-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad64-126">-WhatIf</span></span>
<span data-ttu-id="5ad64-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5ad64-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ad64-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad64-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad64-129">CommonParameters</span></span>
<span data-ttu-id="5ad64-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad64-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad64-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ad64-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad64-132">입력</span><span class="sxs-lookup"><span data-stu-id="5ad64-132">INPUTS</span></span>

### <span data-ttu-id="5ad64-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5ad64-133">System.String</span></span>

## <span data-ttu-id="5ad64-134">출력</span><span class="sxs-lookup"><span data-stu-id="5ad64-134">OUTPUTS</span></span>

### <span data-ttu-id="5ad64-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="5ad64-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="5ad64-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ad64-136">NOTES</span></span>

## <span data-ttu-id="5ad64-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ad64-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ad64-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="5ad64-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="5ad64-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="5ad64-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="5ad64-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5ad64-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5ad64-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5ad64-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="5ad64-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5ad64-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)