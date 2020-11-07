---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878409"
---
# <span data-ttu-id="e53c6-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e53c6-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="e53c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e53c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e53c6-103">리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-103">Gets a resource lock.</span></span>

## <span data-ttu-id="e53c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e53c6-104">SYNTAX</span></span>

### <span data-ttu-id="e53c6-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e53c6-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53c6-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e53c6-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e53c6-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="e53c6-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53c6-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e53c6-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53c6-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e53c6-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53c6-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e53c6-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e53c6-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="e53c6-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e53c6-112">설명은</span><span class="sxs-lookup"><span data-stu-id="e53c6-112">DESCRIPTION</span></span>
<span data-ttu-id="e53c6-113">**Get-AzResourceLock** Cmdlet은 Azure 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="e53c6-114">예제의</span><span class="sxs-lookup"><span data-stu-id="e53c6-114">EXAMPLES</span></span>

### <span data-ttu-id="e53c6-115">예제 1: 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="e53c6-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e53c6-116">이 명령은 ContosoSiteLock 이라는 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="e53c6-117">예제 2: 리소스 그룹 수준 이상에서 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="e53c6-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="e53c6-118">이 명령은 리소스 그룹 또는 구독에 대 한 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="e53c6-119">변수</span><span class="sxs-lookup"><span data-stu-id="e53c6-119">PARAMETERS</span></span>

### <span data-ttu-id="e53c6-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e53c6-120">-ApiVersion</span></span>
<span data-ttu-id="e53c6-121">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e53c6-122">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e53c6-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="e53c6-123">-AtScope</span></span>
<span data-ttu-id="e53c6-124">이 cmdlet이 지정 된 범위 또는 그 위의 모든 잠금을 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="e53c6-125">이 매개 변수를 지정 하지 않으면 cmdlet이 범위 위 또는 아래에 있는 모든 잠금을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="e53c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53c6-126">-DefaultProfile</span></span>
<span data-ttu-id="e53c6-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e53c6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e53c6-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="e53c6-128">-LockId</span></span>
<span data-ttu-id="e53c6-129">이 cmdlet이 가져오는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e53c6-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="e53c6-130">-LockName</span></span>
<span data-ttu-id="e53c6-131">이 cmdlet이 가져오는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53c6-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e53c6-132">-Pre</span></span>
<span data-ttu-id="e53c6-133">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e53c6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53c6-134">-ResourceGroupName</span></span>
<span data-ttu-id="e53c6-135">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="e53c6-136">이 cmdlet은이 리소스 그룹에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="e53c6-137">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="e53c6-137">-ResourceName</span></span>
<span data-ttu-id="e53c6-138">이 잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="e53c6-139">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-139">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53c6-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e53c6-140">-ResourceType</span></span>
<span data-ttu-id="e53c6-141">이 잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="e53c6-142">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-142">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53c6-143">-범위</span><span class="sxs-lookup"><span data-stu-id="e53c6-143">-Scope</span></span>
<span data-ttu-id="e53c6-144">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="e53c6-145">Cmdlet은이 범위에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="e53c6-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e53c6-146">-TenantLevel</span></span>
<span data-ttu-id="e53c6-147">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e53c6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53c6-148">CommonParameters</span></span>
<span data-ttu-id="e53c6-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e53c6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53c6-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e53c6-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53c6-151">입력</span><span class="sxs-lookup"><span data-stu-id="e53c6-151">INPUTS</span></span>

### <span data-ttu-id="e53c6-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e53c6-152">System.String</span></span>

## <span data-ttu-id="e53c6-153">출력</span><span class="sxs-lookup"><span data-stu-id="e53c6-153">OUTPUTS</span></span>

### <span data-ttu-id="e53c6-154">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="e53c6-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e53c6-155">상속자</span><span class="sxs-lookup"><span data-stu-id="e53c6-155">NOTES</span></span>

## <span data-ttu-id="e53c6-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e53c6-156">RELATED LINKS</span></span>

[<span data-ttu-id="e53c6-157">새로운 AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e53c6-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="e53c6-158">제거-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e53c6-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="e53c6-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e53c6-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


