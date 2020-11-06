---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532983"
---
# <span data-ttu-id="77fd1-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="77fd1-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="77fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="77fd1-103">리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77fd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77fd1-104">SYNTAX</span></span>

### <span data-ttu-id="77fd1-105">리소스 그룹 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77fd1-106">리소스 그룹 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77fd1-107">지정 된 범위에 있는 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77fd1-108">구독 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77fd1-109">구독 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77fd1-110">테 넌 트 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77fd1-111">잠금 (Id 기준)</span><span class="sxs-lookup"><span data-stu-id="77fd1-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="77fd1-112">설명은</span><span class="sxs-lookup"><span data-stu-id="77fd1-112">DESCRIPTION</span></span>
<span data-ttu-id="77fd1-113">**Get-AzureRmResourceLock** Cmdlet은 Azure 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="77fd1-114">예제의</span><span class="sxs-lookup"><span data-stu-id="77fd1-114">EXAMPLES</span></span>

### <span data-ttu-id="77fd1-115">예제 1: 잠금 가져오기</span><span class="sxs-lookup"><span data-stu-id="77fd1-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="77fd1-116">이 명령은 ContosoSiteLock 이라는 리소스 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="77fd1-117">변수</span><span class="sxs-lookup"><span data-stu-id="77fd1-117">PARAMETERS</span></span>

### <span data-ttu-id="77fd1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="77fd1-118">-ApiVersion</span></span>
<span data-ttu-id="77fd1-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="77fd1-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="77fd1-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="77fd1-121">-AtScope</span></span>
<span data-ttu-id="77fd1-122">이 cmdlet이 지정 된 범위 또는 그 위의 모든 잠금을 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="77fd1-123">이 매개 변수를 지정 하지 않으면 cmdlet이 범위 위 또는 아래에 있는 모든 잠금을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="77fd1-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="77fd1-124">-InformationAction</span></span>
<span data-ttu-id="77fd1-125">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="77fd1-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77fd1-127">하기로</span><span class="sxs-lookup"><span data-stu-id="77fd1-127">Continue</span></span>
- <span data-ttu-id="77fd1-128">숨기기</span><span class="sxs-lookup"><span data-stu-id="77fd1-128">Ignore</span></span>
- <span data-ttu-id="77fd1-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="77fd1-129">Inquire</span></span>
- <span data-ttu-id="77fd1-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="77fd1-130">SilentlyContinue</span></span>
- <span data-ttu-id="77fd1-131">중지가</span><span class="sxs-lookup"><span data-stu-id="77fd1-131">Stop</span></span>
- <span data-ttu-id="77fd1-132">대기</span><span class="sxs-lookup"><span data-stu-id="77fd1-132">Suspend</span></span>

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

### <span data-ttu-id="77fd1-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="77fd1-133">-InformationVariable</span></span>
<span data-ttu-id="77fd1-134">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="77fd1-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="77fd1-135">-LockId</span></span>
<span data-ttu-id="77fd1-136">이 cmdlet이 가져오는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-137">-LockName</span><span class="sxs-lookup"><span data-stu-id="77fd1-137">-LockName</span></span>
<span data-ttu-id="77fd1-138">이 cmdlet이 가져오는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="77fd1-139">-Pre</span></span>
<span data-ttu-id="77fd1-140">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="77fd1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77fd1-141">-ResourceGroupName</span></span>
<span data-ttu-id="77fd1-142">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="77fd1-143">이 cmdlet은이 리소스 그룹에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-143">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-144">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="77fd1-144">-ResourceName</span></span>
<span data-ttu-id="77fd1-145">이 잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="77fd1-146">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-146">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="77fd1-147">-ResourceType</span></span>
<span data-ttu-id="77fd1-148">이 잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="77fd1-149">이 cmdlet은이 리소스에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-149">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-150">-범위</span><span class="sxs-lookup"><span data-stu-id="77fd1-150">-Scope</span></span>
<span data-ttu-id="77fd1-151">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="77fd1-152">Cmdlet은이 범위에 대 한 잠금을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-152">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="77fd1-153">-TenantLevel</span></span>
<span data-ttu-id="77fd1-154">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-154">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fd1-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fd1-155">-DefaultProfile</span></span>
<span data-ttu-id="77fd1-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77fd1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fd1-157">CommonParameters</span></span>
<span data-ttu-id="77fd1-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fd1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fd1-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77fd1-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fd1-160">입력</span><span class="sxs-lookup"><span data-stu-id="77fd1-160">INPUTS</span></span>

## <span data-ttu-id="77fd1-161">출력</span><span class="sxs-lookup"><span data-stu-id="77fd1-161">OUTPUTS</span></span>

### <span data-ttu-id="77fd1-162">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="77fd1-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="77fd1-163">상속자</span><span class="sxs-lookup"><span data-stu-id="77fd1-163">NOTES</span></span>

## <span data-ttu-id="77fd1-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77fd1-164">RELATED LINKS</span></span>

[<span data-ttu-id="77fd1-165">새로운 AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="77fd1-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="77fd1-166">제거-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="77fd1-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="77fd1-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="77fd1-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


