---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: edc6ac0a9fd98b2876bc320f392e9038fb76741a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993281"
---
# <span data-ttu-id="3c9d4-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3c9d4-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="3c9d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9d4-103">특정 사용자에 대해 Azure AD만 인증을 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="3c9d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c9d4-104">SYNTAX</span></span>

### <span data-ttu-id="3c9d4-105">UseResourceGroupAndServerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c9d4-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c9d4-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c9d4-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c9d4-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c9d4-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c9d4-108">설명</span><span class="sxs-lookup"><span data-stu-id="3c9d4-108">DESCRIPTION</span></span>
<span data-ttu-id="3c9d4-109">**Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet을 사용하면 Azure AD(Azure Active Directory) 현재 구독에서 AzureSQL Server에 대한 인증 요구 사항만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="3c9d4-110">예제</span><span class="sxs-lookup"><span data-stu-id="3c9d4-110">EXAMPLES</span></span>

### <span data-ttu-id="3c9d4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c9d4-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="3c9d4-112">이 명령은 ResourceGroup01이라는 리소스 그룹과 연결된 Server01이라는 AzureSQL 서버에 대해 Azure AD(Azure Active Directory) 인증 요구 사항만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3c9d4-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3c9d4-113">PARAMETERS</span></span>

### <span data-ttu-id="3c9d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9d4-114">-DefaultProfile</span></span>
<span data-ttu-id="3c9d4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c9d4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c9d4-116">-InputObject</span></span>
<span data-ttu-id="3c9d4-117">사용할 SQL 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="3c9d4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c9d4-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c9d4-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c9d4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c9d4-120">-ResourceId</span></span>
<span data-ttu-id="3c9d4-121">사용할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="3c9d4-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="3c9d4-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c9d4-122">-ServerName</span></span>
<span data-ttu-id="3c9d4-123">Azure Active Directory SQL Server 인증에 있는 Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="3c9d4-124">-확인</span><span class="sxs-lookup"><span data-stu-id="3c9d4-124">-Confirm</span></span>
<span data-ttu-id="3c9d4-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c9d4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c9d4-126">-WhatIf</span></span>
<span data-ttu-id="3c9d4-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c9d4-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c9d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9d4-129">CommonParameters</span></span>
<span data-ttu-id="3c9d4-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c9d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9d4-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c9d4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9d4-132">입력</span><span class="sxs-lookup"><span data-stu-id="3c9d4-132">INPUTS</span></span>

### <span data-ttu-id="3c9d4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3c9d4-133">System.String</span></span>

## <span data-ttu-id="3c9d4-134">출력</span><span class="sxs-lookup"><span data-stu-id="3c9d4-134">OUTPUTS</span></span>

### <span data-ttu-id="3c9d4-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="3c9d4-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="3c9d4-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c9d4-136">NOTES</span></span>

## <span data-ttu-id="3c9d4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c9d4-137">RELATED LINKS</span></span>

[<span data-ttu-id="3c9d4-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3c9d4-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3c9d4-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3c9d4-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3c9d4-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3c9d4-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3c9d4-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3c9d4-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3c9d4-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="3c9d4-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)