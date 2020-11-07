---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869245"
---
# <span data-ttu-id="687e4-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="687e4-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="687e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="687e4-102">SYNOPSIS</span></span>
<span data-ttu-id="687e4-103">구독에 청사진 정의를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="687e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="687e4-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687e4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="687e4-105">DESCRIPTION</span></span>
<span data-ttu-id="687e4-106">구독에 청사진 정의를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="687e4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="687e4-107">EXAMPLES</span></span>

### <span data-ttu-id="687e4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="687e4-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="687e4-109">`$blueprintObject`정의 된 매개 변수 및 리소스 그룹 사전을 사용 하 여 지정 된 구독 내에서 청사진 정의에 대 한 새 청사진 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="687e4-110">시스템 할당 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-110">Uses system-assigned identity.</span></span> <span data-ttu-id="687e4-111">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="687e4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="687e4-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="687e4-113">정의 된 매개 변수 및 리소스 그룹 사전을 사용 하 여 지정 된 구독 내에 청사진 정의에 대 한 새 청사진 과제를 만들고 리소스 `$blueprintObject` 잠금을 **allresources** 로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="687e4-114">시스템 할당 id를 사용 하는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="687e4-115">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="687e4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="687e4-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="687e4-117">`$blueprintObject`지정 된 사용자 할당 id id를 사용 하 여 정의 된 매개 변수 및 리소스 그룹 사전을 사용 하 여 지정한 구독에서 청사진 정의에 대 한 새 청사진 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="687e4-118">변수</span><span class="sxs-lookup"><span data-stu-id="687e4-118">PARAMETERS</span></span>

### <span data-ttu-id="687e4-119">-청사진</span><span class="sxs-lookup"><span data-stu-id="687e4-119">-Blueprint</span></span>
<span data-ttu-id="687e4-120">청사진 정의 개체</span><span class="sxs-lookup"><span data-stu-id="687e4-120">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687e4-121">-DefaultProfile</span></span>
<span data-ttu-id="687e4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687e4-123">-위치</span><span class="sxs-lookup"><span data-stu-id="687e4-123">-Location</span></span>
<span data-ttu-id="687e4-124">에서 만들 관리 되는 id의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="687e4-125">자세한 정보 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="687e4-125">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-126">-잠금</span><span class="sxs-lookup"><span data-stu-id="687e4-126">-Lock</span></span>
<span data-ttu-id="687e4-127">리소스 잠그기.</span><span class="sxs-lookup"><span data-stu-id="687e4-127">Lock resources.</span></span>
<span data-ttu-id="687e4-128">자세한 정보 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="687e4-128">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-129">-이름</span><span class="sxs-lookup"><span data-stu-id="687e4-129">-Name</span></span>
<span data-ttu-id="687e4-130">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="687e4-130">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-131">-Parameter</span><span class="sxs-lookup"><span data-stu-id="687e4-131">-Parameter</span></span>
<span data-ttu-id="687e4-132">아티팩트 매개 변수</span><span class="sxs-lookup"><span data-stu-id="687e4-132">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="687e4-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="687e4-134">{{ResourceGroupParameter 매개 변수 설명}}</span><span class="sxs-lookup"><span data-stu-id="687e4-134">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-135">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="687e4-135">-SecureStringParameter</span></span>
<span data-ttu-id="687e4-136">KeyVault 리소스 id, 이름 및 버전에 대 한 보안 문자열 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="687e4-137">-SubscriptionId</span></span>
<span data-ttu-id="687e4-138">청사진 정의를 할당 하는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="687e4-139">SubscriptionId 문자열의 쉼표로 구분 된 목록이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-139">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="687e4-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="687e4-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="687e4-141">시스템 할당 id (MSI)를 통해 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="687e4-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="687e4-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="687e4-143">사용자가 할당 한 id (MSI)를 사용 하 여 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="687e4-144">-확인</span><span class="sxs-lookup"><span data-stu-id="687e4-144">-Confirm</span></span>
<span data-ttu-id="687e4-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687e4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687e4-146">-WhatIf</span></span>
<span data-ttu-id="687e4-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="687e4-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687e4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687e4-149">CommonParameters</span></span>
<span data-ttu-id="687e4-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="687e4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687e4-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="687e4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687e4-152">입력</span><span class="sxs-lookup"><span data-stu-id="687e4-152">INPUTS</span></span>

### <span data-ttu-id="687e4-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="687e4-153">System.String</span></span>

### <span data-ttu-id="687e4-154">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="687e4-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="687e4-155">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="687e4-155">System.String[]</span></span>

### <span data-ttu-id="687e4-156">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="687e4-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="687e4-157">출력</span><span class="sxs-lookup"><span data-stu-id="687e4-157">OUTPUTS</span></span>

### <span data-ttu-id="687e4-158">System. 개체</span><span class="sxs-lookup"><span data-stu-id="687e4-158">System.Object</span></span>
## <span data-ttu-id="687e4-159">상속자</span><span class="sxs-lookup"><span data-stu-id="687e4-159">NOTES</span></span>

## <span data-ttu-id="687e4-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="687e4-160">RELATED LINKS</span></span>
