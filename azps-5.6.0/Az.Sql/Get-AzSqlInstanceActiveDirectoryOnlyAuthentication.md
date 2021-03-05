---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0a06eae51b074cefb74b2ef3a175a056cc52ff84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014544"
---
# <span data-ttu-id="39ff8-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="39ff8-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="39ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="39ff8-103">특정 Managed Instance에 대한 Azure AD SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="39ff8-104">구문</span><span class="sxs-lookup"><span data-stu-id="39ff8-104">SYNTAX</span></span>

### <span data-ttu-id="39ff8-105">UseResourceGroupAndInstanceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="39ff8-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ff8-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39ff8-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ff8-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39ff8-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ff8-108">설명</span><span class="sxs-lookup"><span data-stu-id="39ff8-108">DESCRIPTION</span></span>
<span data-ttu-id="39ff8-109">**Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet은 현재 구독에서 AzureSQL Managed Instance에 대한 Azure Active Directory(Azure ACTIVE Directory) 인증 요구 사항만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="39ff8-110">예제</span><span class="sxs-lookup"><span data-stu-id="39ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="39ff8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="39ff8-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="39ff8-112">이 명령은 ResourceGroup01이라는 리소스 그룹과 연결된 ManagedInstance01이라는 AzureSQL Managed Instance에만 Azure AD(Azure Active Directory) 인증 요구 사항을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="39ff8-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="39ff8-113">PARAMETERS</span></span>

### <span data-ttu-id="39ff8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ff8-114">-DefaultProfile</span></span>
<span data-ttu-id="39ff8-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39ff8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39ff8-116">-InputObject</span></span>
<span data-ttu-id="39ff8-117">사용할 관리되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="39ff8-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="39ff8-118">-InstanceName</span></span>
<span data-ttu-id="39ff8-119">Azure SQL Azure Active Directory만 인증에 있는 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="39ff8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ff8-120">-ResourceGroupName</span></span>
<span data-ttu-id="39ff8-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="39ff8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39ff8-122">-ResourceId</span></span>
<span data-ttu-id="39ff8-123">사용할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="39ff8-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="39ff8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="39ff8-124">-Confirm</span></span>
<span data-ttu-id="39ff8-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ff8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ff8-126">-WhatIf</span></span>
<span data-ttu-id="39ff8-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ff8-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ff8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ff8-129">CommonParameters</span></span>
<span data-ttu-id="39ff8-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39ff8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ff8-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39ff8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ff8-132">입력</span><span class="sxs-lookup"><span data-stu-id="39ff8-132">INPUTS</span></span>

### <span data-ttu-id="39ff8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="39ff8-133">System.String</span></span>

## <span data-ttu-id="39ff8-134">출력</span><span class="sxs-lookup"><span data-stu-id="39ff8-134">OUTPUTS</span></span>

### <span data-ttu-id="39ff8-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="39ff8-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="39ff8-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39ff8-136">NOTES</span></span>

## <span data-ttu-id="39ff8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39ff8-137">RELATED LINKS</span></span>

[<span data-ttu-id="39ff8-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="39ff8-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="39ff8-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="39ff8-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="39ff8-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="39ff8-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="39ff8-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="39ff8-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

