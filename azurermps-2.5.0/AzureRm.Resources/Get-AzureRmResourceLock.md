---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881721"
---
# <span data-ttu-id="a26cf-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a26cf-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="a26cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a26cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a26cf-103">리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a26cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a26cf-104">SYNTAX</span></span>

### <span data-ttu-id="a26cf-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a26cf-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a26cf-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="a26cf-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a26cf-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="a26cf-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a26cf-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="a26cf-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a26cf-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a26cf-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a26cf-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a26cf-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a26cf-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="a26cf-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a26cf-112">설명은</span><span class="sxs-lookup"><span data-stu-id="a26cf-112">DESCRIPTION</span></span>
<span data-ttu-id="a26cf-113">**Get-AzureRmResourceLock** Cmdlet은 Azure 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="a26cf-114">예제의</span><span class="sxs-lookup"><span data-stu-id="a26cf-114">EXAMPLES</span></span>

### <span data-ttu-id="a26cf-115">예제 1: 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="a26cf-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a26cf-116">이 명령은 ContosoSiteLock 이라는 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="a26cf-117">변수</span><span class="sxs-lookup"><span data-stu-id="a26cf-117">PARAMETERS</span></span>

### <span data-ttu-id="a26cf-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a26cf-118">-ApiVersion</span></span>
<span data-ttu-id="a26cf-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a26cf-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a26cf-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="a26cf-121">-AtScope</span></span>
<span data-ttu-id="a26cf-122">이 cmdlet이 지정 된 범위 또는 그 위의 모든 잠금을 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="a26cf-123">이 매개 변수를 지정 하지 않으면 cmdlet이 범위 위 또는 아래에 있는 모든 잠금을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="a26cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26cf-124">-DefaultProfile</span></span>
<span data-ttu-id="a26cf-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a26cf-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26cf-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a26cf-126">-InformationAction</span></span>
<span data-ttu-id="a26cf-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a26cf-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a26cf-129">하기로</span><span class="sxs-lookup"><span data-stu-id="a26cf-129">Continue</span></span>
- <span data-ttu-id="a26cf-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="a26cf-130">Ignore</span></span>
- <span data-ttu-id="a26cf-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="a26cf-131">Inquire</span></span>
- <span data-ttu-id="a26cf-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a26cf-132">SilentlyContinue</span></span>
- <span data-ttu-id="a26cf-133">중지가</span><span class="sxs-lookup"><span data-stu-id="a26cf-133">Stop</span></span>
- <span data-ttu-id="a26cf-134">대기</span><span class="sxs-lookup"><span data-stu-id="a26cf-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26cf-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a26cf-135">-InformationVariable</span></span>
<span data-ttu-id="a26cf-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26cf-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="a26cf-137">-LockId</span></span>
<span data-ttu-id="a26cf-138">이 cmdlet이 가져오는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a26cf-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="a26cf-139">-LockName</span></span>
<span data-ttu-id="a26cf-140">이 cmdlet이 가져오는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a26cf-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="a26cf-141">-Pre</span></span>
<span data-ttu-id="a26cf-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a26cf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26cf-143">-ResourceGroupName</span></span>
<span data-ttu-id="a26cf-144">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="a26cf-145">이 cmdlet은이 리소스 그룹에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="a26cf-146">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="a26cf-146">-ResourceName</span></span>
<span data-ttu-id="a26cf-147">이 잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="a26cf-148">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="a26cf-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a26cf-149">-ResourceType</span></span>
<span data-ttu-id="a26cf-150">이 잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="a26cf-151">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="a26cf-152">-범위</span><span class="sxs-lookup"><span data-stu-id="a26cf-152">-Scope</span></span>
<span data-ttu-id="a26cf-153">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a26cf-154">Cmdlet은이 범위에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="a26cf-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a26cf-155">-TenantLevel</span></span>
<span data-ttu-id="a26cf-156">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a26cf-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26cf-157">CommonParameters</span></span>
<span data-ttu-id="a26cf-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a26cf-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26cf-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a26cf-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26cf-160">입력</span><span class="sxs-lookup"><span data-stu-id="a26cf-160">INPUTS</span></span>

## <span data-ttu-id="a26cf-161">출력</span><span class="sxs-lookup"><span data-stu-id="a26cf-161">OUTPUTS</span></span>

## <span data-ttu-id="a26cf-162">상속자</span><span class="sxs-lookup"><span data-stu-id="a26cf-162">NOTES</span></span>

## <span data-ttu-id="a26cf-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a26cf-163">RELATED LINKS</span></span>

[<span data-ttu-id="a26cf-164">새로운 AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a26cf-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="a26cf-165">제거-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a26cf-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="a26cf-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a26cf-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


