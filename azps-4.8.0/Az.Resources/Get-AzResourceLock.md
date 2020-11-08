---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212174"
---
# <span data-ttu-id="19632-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="19632-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="19632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19632-102">SYNOPSIS</span></span>
<span data-ttu-id="19632-103">리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-103">Gets a resource lock.</span></span>

## <span data-ttu-id="19632-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19632-104">SYNTAX</span></span>

### <span data-ttu-id="19632-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19632-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19632-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="19632-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19632-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="19632-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19632-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="19632-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19632-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="19632-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19632-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="19632-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19632-111">설명은</span><span class="sxs-lookup"><span data-stu-id="19632-111">DESCRIPTION</span></span>
<span data-ttu-id="19632-112">**Get-AzResourceLock** Cmdlet은 Azure 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="19632-113">예제의</span><span class="sxs-lookup"><span data-stu-id="19632-113">EXAMPLES</span></span>

### <span data-ttu-id="19632-114">예제 1: 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="19632-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="19632-115">이 명령은 ContosoSiteLock 이라는 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="19632-116">예제 2: 리소스 그룹 수준 이상에서 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="19632-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="19632-117">이 명령은 리소스 그룹 또는 구독에 대 한 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="19632-118">변수</span><span class="sxs-lookup"><span data-stu-id="19632-118">PARAMETERS</span></span>

### <span data-ttu-id="19632-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19632-119">-ApiVersion</span></span>
<span data-ttu-id="19632-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="19632-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="19632-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="19632-122">-AtScope</span></span>
<span data-ttu-id="19632-123">이 cmdlet이 지정 된 범위 또는 그 위의 모든 잠금을 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19632-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="19632-124">이 매개 변수를 지정 하지 않으면 cmdlet이 범위 위 또는 아래에 있는 모든 잠금을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="19632-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19632-125">-DefaultProfile</span></span>
<span data-ttu-id="19632-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="19632-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19632-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="19632-127">-LockId</span></span>
<span data-ttu-id="19632-128">이 cmdlet이 가져오는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19632-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="19632-129">-LockName</span></span>
<span data-ttu-id="19632-130">이 cmdlet이 가져오는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-130">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19632-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="19632-131">-Pre</span></span>
<span data-ttu-id="19632-132">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="19632-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="19632-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19632-133">-ResourceGroupName</span></span>
<span data-ttu-id="19632-134">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="19632-135">이 cmdlet은이 리소스 그룹에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="19632-136">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="19632-136">-ResourceName</span></span>
<span data-ttu-id="19632-137">이 잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="19632-138">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="19632-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="19632-139">-ResourceType</span></span>
<span data-ttu-id="19632-140">이 잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="19632-141">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="19632-142">-범위</span><span class="sxs-lookup"><span data-stu-id="19632-142">-Scope</span></span>
<span data-ttu-id="19632-143">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="19632-144">Cmdlet은이 범위에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19632-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="19632-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19632-145">CommonParameters</span></span>
<span data-ttu-id="19632-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19632-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19632-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19632-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19632-148">입력</span><span class="sxs-lookup"><span data-stu-id="19632-148">INPUTS</span></span>

### <span data-ttu-id="19632-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19632-149">System.String</span></span>

## <span data-ttu-id="19632-150">출력</span><span class="sxs-lookup"><span data-stu-id="19632-150">OUTPUTS</span></span>

### <span data-ttu-id="19632-151">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="19632-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19632-152">상속자</span><span class="sxs-lookup"><span data-stu-id="19632-152">NOTES</span></span>

## <span data-ttu-id="19632-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19632-153">RELATED LINKS</span></span>

[<span data-ttu-id="19632-154">새로운 AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="19632-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="19632-155">제거-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="19632-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="19632-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="19632-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


