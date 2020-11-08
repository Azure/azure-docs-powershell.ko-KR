---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213259"
---
# <span data-ttu-id="65ecf-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="65ecf-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="65ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="65ecf-103">특정 SQL 관리 인스턴스에 대 한 Azure AD 전용 인증을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="65ecf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65ecf-104">SYNTAX</span></span>

### <span data-ttu-id="65ecf-105">UseResourceGroupAndInstanceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="65ecf-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ecf-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65ecf-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ecf-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65ecf-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ecf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="65ecf-108">DESCRIPTION</span></span>
<span data-ttu-id="65ecf-109">**AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet은 현재 구독의 AzureSQL 관리 인스턴스에 대 한 azure AD (Azure Active Directory) 인증 요구 사항만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="65ecf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="65ecf-110">EXAMPLES</span></span>

### <span data-ttu-id="65ecf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="65ecf-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="65ecf-112">이 명령은 ResourceGroup01 이라는 리소스 그룹과 연결 된 ManagedInstance01 라는 AzureSQL 관리 되는 인스턴스에 대 한 azure AD (Azure Active Directory) 인증 요구 사항만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="65ecf-113">변수</span><span class="sxs-lookup"><span data-stu-id="65ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="65ecf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ecf-114">-DefaultProfile</span></span>
<span data-ttu-id="65ecf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ecf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65ecf-116">-InputObject</span></span>
<span data-ttu-id="65ecf-117">사용할 관리 되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ecf-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="65ecf-118">-InstanceName</span></span>
<span data-ttu-id="65ecf-119">Azure Active Directory만 인증을 하는 Azure SQL 관리 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ecf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ecf-120">-ResourceGroupName</span></span>
<span data-ttu-id="65ecf-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ecf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65ecf-122">-ResourceId</span></span>
<span data-ttu-id="65ecf-123">사용할 인스턴스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="65ecf-124">-확인</span><span class="sxs-lookup"><span data-stu-id="65ecf-124">-Confirm</span></span>
<span data-ttu-id="65ecf-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ecf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ecf-126">-WhatIf</span></span>
<span data-ttu-id="65ecf-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ecf-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ecf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ecf-129">CommonParameters</span></span>
<span data-ttu-id="65ecf-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65ecf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ecf-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="65ecf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ecf-132">입력</span><span class="sxs-lookup"><span data-stu-id="65ecf-132">INPUTS</span></span>

### <span data-ttu-id="65ecf-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65ecf-133">System.String</span></span>

## <span data-ttu-id="65ecf-134">출력</span><span class="sxs-lookup"><span data-stu-id="65ecf-134">OUTPUTS</span></span>

### <span data-ttu-id="65ecf-135">InstanceActiveDirectoryOnlyAuthentication. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="65ecf-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="65ecf-136">상속자</span><span class="sxs-lookup"><span data-stu-id="65ecf-136">NOTES</span></span>

## <span data-ttu-id="65ecf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65ecf-137">RELATED LINKS</span></span>

[<span data-ttu-id="65ecf-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="65ecf-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="65ecf-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="65ecf-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="65ecf-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="65ecf-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="65ecf-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="65ecf-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

