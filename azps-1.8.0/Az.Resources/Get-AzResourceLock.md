---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699417"
---
# <span data-ttu-id="6fc69-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6fc69-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="6fc69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc69-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc69-103">리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-103">Gets a resource lock.</span></span>

## <span data-ttu-id="6fc69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fc69-104">SYNTAX</span></span>

### <span data-ttu-id="6fc69-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6fc69-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc69-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="6fc69-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fc69-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="6fc69-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc69-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="6fc69-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc69-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="6fc69-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc69-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="6fc69-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc69-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="6fc69-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc69-112">설명은</span><span class="sxs-lookup"><span data-stu-id="6fc69-112">DESCRIPTION</span></span>
<span data-ttu-id="6fc69-113">**Get-AzResourceLock** Cmdlet은 Azure 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="6fc69-114">예제의</span><span class="sxs-lookup"><span data-stu-id="6fc69-114">EXAMPLES</span></span>

### <span data-ttu-id="6fc69-115">예제 1: 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="6fc69-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="6fc69-116">이 명령은 ContosoSiteLock 이라는 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="6fc69-117">변수</span><span class="sxs-lookup"><span data-stu-id="6fc69-117">PARAMETERS</span></span>

### <span data-ttu-id="6fc69-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6fc69-118">-ApiVersion</span></span>
<span data-ttu-id="6fc69-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6fc69-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6fc69-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="6fc69-121">-AtScope</span></span>
<span data-ttu-id="6fc69-122">이 cmdlet이 지정 된 범위 또는 그 위의 모든 잠금을 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="6fc69-123">이 매개 변수를 지정 하지 않으면 cmdlet이 범위 위 또는 아래에 있는 모든 잠금을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="6fc69-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc69-124">-DefaultProfile</span></span>
<span data-ttu-id="6fc69-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6fc69-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fc69-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="6fc69-126">-LockId</span></span>
<span data-ttu-id="6fc69-127">이 cmdlet이 가져오는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6fc69-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="6fc69-128">-LockName</span></span>
<span data-ttu-id="6fc69-129">이 cmdlet이 가져오는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6fc69-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="6fc69-130">-Pre</span></span>
<span data-ttu-id="6fc69-131">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6fc69-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc69-132">-ResourceGroupName</span></span>
<span data-ttu-id="6fc69-133">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="6fc69-134">이 cmdlet은이 리소스 그룹에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="6fc69-135">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="6fc69-135">-ResourceName</span></span>
<span data-ttu-id="6fc69-136">이 잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="6fc69-137">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="6fc69-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6fc69-138">-ResourceType</span></span>
<span data-ttu-id="6fc69-139">이 잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="6fc69-140">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="6fc69-141">-범위</span><span class="sxs-lookup"><span data-stu-id="6fc69-141">-Scope</span></span>
<span data-ttu-id="6fc69-142">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="6fc69-143">Cmdlet은이 범위에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="6fc69-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6fc69-144">-TenantLevel</span></span>
<span data-ttu-id="6fc69-145">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6fc69-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc69-146">CommonParameters</span></span>
<span data-ttu-id="6fc69-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fc69-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc69-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc69-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc69-149">입력</span><span class="sxs-lookup"><span data-stu-id="6fc69-149">INPUTS</span></span>

### <span data-ttu-id="6fc69-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fc69-150">System.String</span></span>

## <span data-ttu-id="6fc69-151">출력</span><span class="sxs-lookup"><span data-stu-id="6fc69-151">OUTPUTS</span></span>

### <span data-ttu-id="6fc69-152">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="6fc69-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6fc69-153">상속자</span><span class="sxs-lookup"><span data-stu-id="6fc69-153">NOTES</span></span>

## <span data-ttu-id="6fc69-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fc69-154">RELATED LINKS</span></span>

[<span data-ttu-id="6fc69-155">새로운 AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6fc69-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="6fc69-156">제거-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6fc69-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="6fc69-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="6fc69-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


