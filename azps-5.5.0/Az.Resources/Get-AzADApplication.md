---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178908"
---
# <span data-ttu-id="ed660-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ed660-101">Get-AzADApplication</span></span>

## <span data-ttu-id="ed660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed660-102">SYNOPSIS</span></span>
<span data-ttu-id="ed660-103">기존 Azure Active Directory 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="ed660-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed660-104">SYNTAX</span></span>

### <span data-ttu-id="ed660-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ed660-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ed660-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed660-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ed660-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed660-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ed660-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed660-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ed660-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed660-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ed660-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed660-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ed660-111">설명</span><span class="sxs-lookup"><span data-stu-id="ed660-111">DESCRIPTION</span></span>
<span data-ttu-id="ed660-112">기존 Azure Active Directory 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="ed660-113">Application Lookup은 ObjectId, ApplicationId, IdentifierUri 또는 DisplayName으로 수행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="ed660-114">제공된 매개 변수가 없는 경우 테넌트의 모든 애플리케이션을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="ed660-115">예제</span><span class="sxs-lookup"><span data-stu-id="ed660-115">EXAMPLES</span></span>

### <span data-ttu-id="ed660-116">예제 1 - 모든 애플리케이션 나열</span><span class="sxs-lookup"><span data-stu-id="ed660-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="ed660-117">테넌트의 모든 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="ed660-118">예제 2 - Paging를 사용하여 애플리케이션 나열</span><span class="sxs-lookup"><span data-stu-id="ed660-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="ed660-119">테넌트에서 처음 100개 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="ed660-120">예제 3 - 식별자 URI로 애플리케이션을 얻게</span><span class="sxs-lookup"><span data-stu-id="ed660-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="ed660-121">식별자 URI가 "인 애플리케이션을 http://mySecretApp1 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="ed660-122">예제 4 - 개체 ID로 애플리케이션을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="ed660-123">개체 ID가 '39e64ec6-569b-4030-8e1c-c3c519a05d69'인 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="ed660-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed660-124">PARAMETERS</span></span>

### <span data-ttu-id="ed660-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ed660-125">-ApplicationId</span></span>
<span data-ttu-id="ed660-126">인계할 애플리케이션의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed660-127">-DefaultProfile</span></span>
<span data-ttu-id="ed660-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ed660-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed660-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed660-129">-DisplayName</span></span>
<span data-ttu-id="ed660-130">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="ed660-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="ed660-132">표시 이름으로 시작하는 모든 애플리케이션을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="ed660-133">-IdentifierUri</span></span>
<span data-ttu-id="ed660-134">인계할 애플리케이션의 고유 식별자 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ed660-135">-ObjectId</span></span>
<span data-ttu-id="ed660-136">인계할 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ed660-137">-IncludeTotalCount</span></span>
<span data-ttu-id="ed660-138">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ed660-139">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ed660-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="ed660-140">-Skip</span></span>
<span data-ttu-id="ed660-141">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-141">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-142">-First</span><span class="sxs-lookup"><span data-stu-id="ed660-142">-First</span></span>
<span data-ttu-id="ed660-143">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-143">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed660-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed660-144">CommonParameters</span></span>
<span data-ttu-id="ed660-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed660-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed660-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ed660-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed660-147">입력</span><span class="sxs-lookup"><span data-stu-id="ed660-147">INPUTS</span></span>

### <span data-ttu-id="ed660-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ed660-148">System.String</span></span>

### <span data-ttu-id="ed660-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ed660-149">System.Guid</span></span>

## <span data-ttu-id="ed660-150">출력</span><span class="sxs-lookup"><span data-stu-id="ed660-150">OUTPUTS</span></span>

### <span data-ttu-id="ed660-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ed660-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="ed660-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed660-152">NOTES</span></span>

## <span data-ttu-id="ed660-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed660-153">RELATED LINKS</span></span>

[<span data-ttu-id="ed660-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ed660-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="ed660-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ed660-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="ed660-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ed660-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="ed660-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ed660-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="ed660-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ed660-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="ed660-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ed660-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

