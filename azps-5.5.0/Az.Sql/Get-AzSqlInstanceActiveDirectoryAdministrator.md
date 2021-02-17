---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191076"
---
# <span data-ttu-id="125c7-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="125c7-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="125c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="125c7-102">SYNOPSIS</span></span>
<span data-ttu-id="125c7-103">Managed Instance에 대한 Azure AD SQL 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="125c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="125c7-104">SYNTAX</span></span>

### <span data-ttu-id="125c7-105">UseResourceGroupAndInstanceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="125c7-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="125c7-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="125c7-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="125c7-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="125c7-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="125c7-108">설명</span><span class="sxs-lookup"><span data-stu-id="125c7-108">DESCRIPTION</span></span>
<span data-ttu-id="125c7-109">**Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet은 현재 구독에서 AzureSQL Managed Instance에 대한 Azure AD(Azure Active Directory) 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="125c7-110">예제</span><span class="sxs-lookup"><span data-stu-id="125c7-110">EXAMPLES</span></span>

### <span data-ttu-id="125c7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="125c7-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="125c7-112">이 명령은 ResourceGroup01이라는 리소스 그룹과 연결된 ManagedInstance01이라는 관리되는 인스턴스에 대한 Azure AD 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="125c7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="125c7-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="125c7-114">이 명령은 관리되는 인스턴스 개체에서 Azure AD 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="125c7-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="125c7-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="125c7-116">이 명령은 관리되는 인스턴스 리소스 식별자를 사용하여 Azure AD 관리자에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="125c7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="125c7-117">PARAMETERS</span></span>

### <span data-ttu-id="125c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125c7-118">-DefaultProfile</span></span>
<span data-ttu-id="125c7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="125c7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="125c7-120">-InputObject</span></span>
<span data-ttu-id="125c7-121">사용할 관리되는 인스턴스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="125c7-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="125c7-122">-InstanceName</span></span>
<span data-ttu-id="125c7-123">SQL 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="125c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="125c7-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="125c7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="125c7-126">-ResourceId</span></span>
<span data-ttu-id="125c7-127">사용할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="125c7-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="125c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125c7-128">CommonParameters</span></span>
<span data-ttu-id="125c7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="125c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125c7-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="125c7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125c7-131">입력</span><span class="sxs-lookup"><span data-stu-id="125c7-131">INPUTS</span></span>

### <span data-ttu-id="125c7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="125c7-132">System.String</span></span>

## <span data-ttu-id="125c7-133">출력</span><span class="sxs-lookup"><span data-stu-id="125c7-133">OUTPUTS</span></span>

### <span data-ttu-id="125c7-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="125c7-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="125c7-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="125c7-135">NOTES</span></span>

## <span data-ttu-id="125c7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="125c7-136">RELATED LINKS</span></span>

[<span data-ttu-id="125c7-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="125c7-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="125c7-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="125c7-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
