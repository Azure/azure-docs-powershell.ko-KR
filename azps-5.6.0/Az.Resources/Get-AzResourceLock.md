---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 70c52508bbb152047d40d7556a41ad76e3ca2eac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963776"
---
# <span data-ttu-id="e8ad0-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e8ad0-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="e8ad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ad0-103">리소스 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-103">Gets a resource lock.</span></span>

## <span data-ttu-id="e8ad0-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8ad0-104">SYNTAX</span></span>

### <span data-ttu-id="e8ad0-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8ad0-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ad0-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e8ad0-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8ad0-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="e8ad0-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ad0-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e8ad0-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ad0-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e8ad0-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ad0-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="e8ad0-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ad0-111">설명</span><span class="sxs-lookup"><span data-stu-id="e8ad0-111">DESCRIPTION</span></span>
<span data-ttu-id="e8ad0-112">**Get-AzResourceLock** cmdlet은 Azure 리소스 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="e8ad0-113">예제</span><span class="sxs-lookup"><span data-stu-id="e8ad0-113">EXAMPLES</span></span>

### <span data-ttu-id="e8ad0-114">예제 1: 잠금 해제</span><span class="sxs-lookup"><span data-stu-id="e8ad0-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e8ad0-115">이 명령은 ContosoSiteLock이라는 리소스 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="e8ad0-116">예제 2: 리소스 그룹 수준 이상에서 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="e8ad0-117">이 명령은 리소스 그룹 또는 구독에서 리소스 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="e8ad0-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e8ad0-118">PARAMETERS</span></span>

### <span data-ttu-id="e8ad0-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e8ad0-119">-ApiVersion</span></span>
<span data-ttu-id="e8ad0-120">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e8ad0-121">버전을 지정하지 않으면 이 cmdlet에서는 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e8ad0-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="e8ad0-122">-AtScope</span></span>
<span data-ttu-id="e8ad0-123">이 cmdlet은 지정된 범위 이상에서 모든 잠금을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="e8ad0-124">이 매개 변수를 지정하지 않으면 cmdlet은 범위 위 또는 아래에 있는 모든 잠금을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="e8ad0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ad0-125">-DefaultProfile</span></span>
<span data-ttu-id="e8ad0-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e8ad0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ad0-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="e8ad0-127">-LockId</span></span>
<span data-ttu-id="e8ad0-128">이 cmdlet이 얻을 잠금의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ad0-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="e8ad0-129">-LockName</span></span>
<span data-ttu-id="e8ad0-130">이 cmdlet이 얻을 잠금의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ad0-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="e8ad0-131">-Pre</span></span>
<span data-ttu-id="e8ad0-132">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e8ad0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ad0-133">-ResourceGroupName</span></span>
<span data-ttu-id="e8ad0-134">잠금이 적용되는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="e8ad0-135">이 cmdlet은 이 리소스 그룹에 대한 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-135">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ad0-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e8ad0-136">-ResourceName</span></span>
<span data-ttu-id="e8ad0-137">이 잠금이 적용되는 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="e8ad0-138">이 cmdlet은 이 리소스에 대한 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ad0-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e8ad0-139">-ResourceType</span></span>
<span data-ttu-id="e8ad0-140">이 잠금이 적용되는 리소스의 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="e8ad0-141">이 cmdlet은 이 리소스에 대한 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ad0-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="e8ad0-142">-Scope</span></span>
<span data-ttu-id="e8ad0-143">잠금이 적용되는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="e8ad0-144">cmdlet은 이 범위에 대한 잠금을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-144">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ad0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ad0-145">CommonParameters</span></span>
<span data-ttu-id="e8ad0-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ad0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ad0-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8ad0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ad0-148">입력</span><span class="sxs-lookup"><span data-stu-id="e8ad0-148">INPUTS</span></span>

### <span data-ttu-id="e8ad0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e8ad0-149">System.String</span></span>

## <span data-ttu-id="e8ad0-150">출력</span><span class="sxs-lookup"><span data-stu-id="e8ad0-150">OUTPUTS</span></span>

### <span data-ttu-id="e8ad0-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e8ad0-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e8ad0-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8ad0-152">NOTES</span></span>

## <span data-ttu-id="e8ad0-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8ad0-153">RELATED LINKS</span></span>

[<span data-ttu-id="e8ad0-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e8ad0-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="e8ad0-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e8ad0-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="e8ad0-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e8ad0-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


