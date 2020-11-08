---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214679"
---
# <span data-ttu-id="64820-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="64820-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="64820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64820-102">SYNOPSIS</span></span>
<span data-ttu-id="64820-103">리소스에 대 한 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="64820-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64820-104">SYNTAX</span></span>

### <span data-ttu-id="64820-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="64820-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64820-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="64820-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64820-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="64820-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64820-108">설명은</span><span class="sxs-lookup"><span data-stu-id="64820-108">DESCRIPTION</span></span>
<span data-ttu-id="64820-109">**AzResourceAction** cmdlet은 지정 된 Azure 리소스에 대해 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="64820-110">지원 되는 작업 목록을 보려면 Azure 리소스 탐색기 도구를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="64820-111">예제의</span><span class="sxs-lookup"><span data-stu-id="64820-111">EXAMPLES</span></span>

### <span data-ttu-id="64820-112">예제 1: ResourceId를 사용 하 여 VM 시작 호출</span><span class="sxs-lookup"><span data-stu-id="64820-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="64820-113">이 명령은 {ResourceId}를 사용 하 여 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="64820-114">예제 2: Context.resourcename을 사용 하 여 VM에서 poweroffing 호출</span><span class="sxs-lookup"><span data-stu-id="64820-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="64820-115">이 명령은 가상 컴퓨터에서 {ResourceId}를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="64820-116">명령에서 *Force* 매개 변수를 지정 하므로 확인을 요청 하는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64820-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="64820-117">예제 3: ResourceId를 사용 하 여 리소스 공급자 등록 호출</span><span class="sxs-lookup"><span data-stu-id="64820-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="64820-118">이 명령은 리소스 공급자 "Microsoft. 네트워크"를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="64820-119">명령에서 *Force* 매개 변수를 지정 하므로 확인을 요청 하는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64820-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="64820-120">변수</span><span class="sxs-lookup"><span data-stu-id="64820-120">PARAMETERS</span></span>

### <span data-ttu-id="64820-121">-작업</span><span class="sxs-lookup"><span data-stu-id="64820-121">-Action</span></span>
<span data-ttu-id="64820-122">호출할 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64820-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="64820-123">-ApiVersion</span></span>
<span data-ttu-id="64820-124">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="64820-125">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64820-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64820-126">-DefaultProfile</span></span>
<span data-ttu-id="64820-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="64820-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64820-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="64820-128">-ExtensionResourceName</span></span>
<span data-ttu-id="64820-129">이 cmdlet이 작업을 호출 하는 리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="64820-130">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="64820-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64820-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="64820-131">-ExtensionResourceType</span></span>
<span data-ttu-id="64820-132">확장 리소스의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="64820-133">예를 들면 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="64820-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64820-134">-Force</span><span class="sxs-lookup"><span data-stu-id="64820-134">-Force</span></span>
<span data-ttu-id="64820-135">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64820-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="64820-136">-ODataQuery</span></span>
<span data-ttu-id="64820-137">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="64820-138">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64820-139">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="64820-139">-Parameters</span></span>
<span data-ttu-id="64820-140">이 cmdlet이 호출 하는 작업에 대 한 매개 변수를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64820-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="64820-141">-Pre</span></span>
<span data-ttu-id="64820-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64820-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="64820-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64820-143">-ResourceGroupName</span></span>
<span data-ttu-id="64820-144">이 cmdlet이 동작을 호출 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64820-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64820-145">-ResourceId</span></span>
<span data-ttu-id="64820-146">이 cmdlet이 작업을 호출 하는 리소스의 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="64820-147">ID에는 다음 예제와 같이 구독이 포함 됩니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="64820-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64820-148">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="64820-148">-ResourceName</span></span>
<span data-ttu-id="64820-149">이 cmdlet이 작업을 호출 하는 리소스의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="64820-150">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="64820-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64820-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="64820-151">-ResourceType</span></span>
<span data-ttu-id="64820-152">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="64820-153">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="64820-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64820-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="64820-154">-TenantLevel</span></span>
<span data-ttu-id="64820-155">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64820-155">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64820-156">-확인</span><span class="sxs-lookup"><span data-stu-id="64820-156">-Confirm</span></span>
<span data-ttu-id="64820-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64820-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64820-158">-WhatIf</span></span>
<span data-ttu-id="64820-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64820-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64820-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64820-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64820-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64820-161">CommonParameters</span></span>
<span data-ttu-id="64820-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64820-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64820-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64820-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64820-164">입력</span><span class="sxs-lookup"><span data-stu-id="64820-164">INPUTS</span></span>

### <span data-ttu-id="64820-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64820-165">System.String</span></span>

## <span data-ttu-id="64820-166">출력</span><span class="sxs-lookup"><span data-stu-id="64820-166">OUTPUTS</span></span>

### <span data-ttu-id="64820-167">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="64820-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="64820-168">상속자</span><span class="sxs-lookup"><span data-stu-id="64820-168">NOTES</span></span>

## <span data-ttu-id="64820-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64820-169">RELATED LINKS</span></span>
