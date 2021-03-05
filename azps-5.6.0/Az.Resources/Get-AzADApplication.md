---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 759977fb861f0ff2f1ede1fb28af50448b5ba5ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984187"
---
# <span data-ttu-id="a7d88-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a7d88-101">Get-AzADApplication</span></span>

## <span data-ttu-id="a7d88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d88-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d88-103">기존 Azure Active Directory 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="a7d88-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7d88-104">SYNTAX</span></span>

### <span data-ttu-id="a7d88-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a7d88-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a7d88-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d88-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a7d88-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d88-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a7d88-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d88-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a7d88-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d88-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a7d88-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d88-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a7d88-111">설명</span><span class="sxs-lookup"><span data-stu-id="a7d88-111">DESCRIPTION</span></span>
<span data-ttu-id="a7d88-112">기존 Azure Active Directory 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="a7d88-113">Application lookup은 ObjectId, ApplicationId, IdentifierUri 또는 DisplayName에서 수행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="a7d88-114">매개 변수가 제공되지 않고 테넌트 아래에 있는 모든 애플리케이션을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="a7d88-115">예제</span><span class="sxs-lookup"><span data-stu-id="a7d88-115">EXAMPLES</span></span>

### <span data-ttu-id="a7d88-116">예제 1 - 모든 애플리케이션 나열</span><span class="sxs-lookup"><span data-stu-id="a7d88-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="a7d88-117">테넌트 아래에서 모든 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="a7d88-118">예제 2 - paging를 사용하여 애플리케이션 나열</span><span class="sxs-lookup"><span data-stu-id="a7d88-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="a7d88-119">테넌트 아래에 처음 100개 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="a7d88-120">예제 3 - 식별자 URI로 애플리케이션을 얻다</span><span class="sxs-lookup"><span data-stu-id="a7d88-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="a7d88-121">식별자 uri를 "로 http://mySecretApp1 애플리케이션을 를 습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="a7d88-122">예제 4 - 개체 ID로 애플리케이션을 Get</span><span class="sxs-lookup"><span data-stu-id="a7d88-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="a7d88-123">개체 ID '39e64ec6-569b-4030-8e1c-c3c519a05d69'로 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="a7d88-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7d88-124">PARAMETERS</span></span>

### <span data-ttu-id="a7d88-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a7d88-125">-ApplicationId</span></span>
<span data-ttu-id="a7d88-126">인치할 애플리케이션의 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="a7d88-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d88-127">-DefaultProfile</span></span>
<span data-ttu-id="a7d88-128">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a7d88-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7d88-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a7d88-129">-DisplayName</span></span>
<span data-ttu-id="a7d88-130">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-130">The display name of the application.</span></span>

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

### <span data-ttu-id="a7d88-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="a7d88-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="a7d88-132">표시 이름으로 시작하는 모든 애플리케이션을 인치합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="a7d88-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="a7d88-133">-IdentifierUri</span></span>
<span data-ttu-id="a7d88-134">인치할 애플리케이션의 고유 식별자 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="a7d88-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a7d88-135">-ObjectId</span></span>
<span data-ttu-id="a7d88-136">인치할 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="a7d88-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a7d88-137">-IncludeTotalCount</span></span>
<span data-ttu-id="a7d88-138">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a7d88-139">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a7d88-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="a7d88-140">-Skip</span></span>
<span data-ttu-id="a7d88-141">첫 번째 N 개체를 무시한 다음 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="a7d88-142">-First</span><span class="sxs-lookup"><span data-stu-id="a7d88-142">-First</span></span>
<span data-ttu-id="a7d88-143">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="a7d88-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d88-144">CommonParameters</span></span>
<span data-ttu-id="a7d88-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d88-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d88-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d88-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d88-147">입력</span><span class="sxs-lookup"><span data-stu-id="a7d88-147">INPUTS</span></span>

### <span data-ttu-id="a7d88-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d88-148">System.String</span></span>

### <span data-ttu-id="a7d88-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a7d88-149">System.Guid</span></span>

## <span data-ttu-id="a7d88-150">출력</span><span class="sxs-lookup"><span data-stu-id="a7d88-150">OUTPUTS</span></span>

### <span data-ttu-id="a7d88-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a7d88-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a7d88-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7d88-152">NOTES</span></span>

## <span data-ttu-id="a7d88-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7d88-153">RELATED LINKS</span></span>

[<span data-ttu-id="a7d88-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a7d88-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="a7d88-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a7d88-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="a7d88-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a7d88-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="a7d88-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a7d88-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a7d88-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a7d88-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="a7d88-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a7d88-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

