---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869249"
---
# <span data-ttu-id="42e00-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="42e00-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="42e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e00-102">SYNOPSIS</span></span>
<span data-ttu-id="42e00-103">기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="42e00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42e00-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42e00-105">설명은</span><span class="sxs-lookup"><span data-stu-id="42e00-105">DESCRIPTION</span></span>
<span data-ttu-id="42e00-106">기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="42e00-107">예제의</span><span class="sxs-lookup"><span data-stu-id="42e00-107">EXAMPLES</span></span>

### <span data-ttu-id="42e00-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="42e00-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="42e00-109">지정 된 구독 내에서 청사진 정의에 대 한 기존 청사진 과제 `$blueprintObject` 를 업데이트 하 고 매개 변수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="42e00-110">시스템 할당 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-110">Uses system-assigned identity.</span></span> <span data-ttu-id="42e00-111">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="42e00-112">변수</span><span class="sxs-lookup"><span data-stu-id="42e00-112">PARAMETERS</span></span>

### <span data-ttu-id="42e00-113">-청사진</span><span class="sxs-lookup"><span data-stu-id="42e00-113">-Blueprint</span></span>
<span data-ttu-id="42e00-114">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="42e00-114">Blueprint object.</span></span>

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

### <span data-ttu-id="42e00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e00-115">-DefaultProfile</span></span>
<span data-ttu-id="42e00-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e00-117">-위치</span><span class="sxs-lookup"><span data-stu-id="42e00-117">-Location</span></span>
<span data-ttu-id="42e00-118">에서 만들 관리 되는 id의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="42e00-119">자세한 정보 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="42e00-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="42e00-120">-잠금</span><span class="sxs-lookup"><span data-stu-id="42e00-120">-Lock</span></span>
<span data-ttu-id="42e00-121">리소스 잠그기.</span><span class="sxs-lookup"><span data-stu-id="42e00-121">Lock resources.</span></span>
<span data-ttu-id="42e00-122">자세한 정보 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="42e00-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="42e00-123">-이름</span><span class="sxs-lookup"><span data-stu-id="42e00-123">-Name</span></span>
<span data-ttu-id="42e00-124">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="42e00-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="42e00-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="42e00-125">-Parameter</span></span>
<span data-ttu-id="42e00-126">아티팩트 매개 변수</span><span class="sxs-lookup"><span data-stu-id="42e00-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="42e00-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="42e00-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="42e00-128">{{ResourceGroupParameter 매개 변수 설명}}</span><span class="sxs-lookup"><span data-stu-id="42e00-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="42e00-129">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="42e00-129">-SecureStringParameter</span></span>
<span data-ttu-id="42e00-130">KeyVault 리소스 id, 이름 및 버전에 대 한 보안 문자열 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="42e00-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42e00-131">-SubscriptionId</span></span>
<span data-ttu-id="42e00-132">SubscriptionId는 청사진을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="42e00-133">SubscriptionId 문자열의 쉼표로 구분 된 목록이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="42e00-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="42e00-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="42e00-135">시스템 할당 id (MSI)를 통해 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="42e00-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="42e00-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="42e00-137">사용자가 할당 한 id (MSI)를 사용 하 여 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e00-138">-확인</span><span class="sxs-lookup"><span data-stu-id="42e00-138">-Confirm</span></span>
<span data-ttu-id="42e00-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e00-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e00-140">-WhatIf</span></span>
<span data-ttu-id="42e00-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e00-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e00-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e00-143">CommonParameters</span></span>
<span data-ttu-id="42e00-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42e00-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e00-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e00-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e00-146">입력</span><span class="sxs-lookup"><span data-stu-id="42e00-146">INPUTS</span></span>

### <span data-ttu-id="42e00-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42e00-147">System.String</span></span>

### <span data-ttu-id="42e00-148">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="42e00-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="42e00-149">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="42e00-149">System.String[]</span></span>

### <span data-ttu-id="42e00-150">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="42e00-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="42e00-151">출력</span><span class="sxs-lookup"><span data-stu-id="42e00-151">OUTPUTS</span></span>

### <span data-ttu-id="42e00-152">System. 개체</span><span class="sxs-lookup"><span data-stu-id="42e00-152">System.Object</span></span>
## <span data-ttu-id="42e00-153">상속자</span><span class="sxs-lookup"><span data-stu-id="42e00-153">NOTES</span></span>

## <span data-ttu-id="42e00-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42e00-154">RELATED LINKS</span></span>
