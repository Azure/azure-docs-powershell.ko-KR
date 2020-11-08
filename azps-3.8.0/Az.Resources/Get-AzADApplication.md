---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: afcb95eca70c005023bacc2b2d71d9fda54c9259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042031"
---
# <span data-ttu-id="77fbb-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="77fbb-101">Get-AzADApplication</span></span>

## <span data-ttu-id="77fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="77fbb-103">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="77fbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77fbb-104">SYNTAX</span></span>

### <span data-ttu-id="77fbb-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="77fbb-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="77fbb-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fbb-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="77fbb-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fbb-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="77fbb-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fbb-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="77fbb-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fbb-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="77fbb-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fbb-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="77fbb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="77fbb-111">DESCRIPTION</span></span>
<span data-ttu-id="77fbb-112">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="77fbb-113">Application lookup은 ObjectId, ApplicationId, IdentifierUri 또는 DisplayName으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="77fbb-114">매개 변수를 제공 하지 않으면 테 넌 트 아래의 모든 응용 프로그램을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="77fbb-115">예제의</span><span class="sxs-lookup"><span data-stu-id="77fbb-115">EXAMPLES</span></span>

### <span data-ttu-id="77fbb-116">예제 1-모든 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="77fbb-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="77fbb-117">테 넌 트 아래에 모든 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="77fbb-118">예제 2-페이징을 사용 하 여 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="77fbb-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="77fbb-119">테 넌 트 아래 첫 번째 100 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="77fbb-120">예제 3-식별자 URI로 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="77fbb-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="77fbb-121">식별자 uri를 사용 하는 응용 프로그램을 ""로 가져옵니다 http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="77fbb-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="77fbb-122">예제 4-개체 id 별 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="77fbb-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="77fbb-123">개체 id가 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' 인 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="77fbb-124">변수</span><span class="sxs-lookup"><span data-stu-id="77fbb-124">PARAMETERS</span></span>

### <span data-ttu-id="77fbb-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="77fbb-125">-ApplicationId</span></span>
<span data-ttu-id="77fbb-126">가져올 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="77fbb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fbb-127">-DefaultProfile</span></span>
<span data-ttu-id="77fbb-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="77fbb-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77fbb-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="77fbb-129">-DisplayName</span></span>
<span data-ttu-id="77fbb-130">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-130">The display name of the application.</span></span>

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

### <span data-ttu-id="77fbb-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="77fbb-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="77fbb-132">표시 이름으로 시작 하는 모든 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="77fbb-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="77fbb-133">-IdentifierUri</span></span>
<span data-ttu-id="77fbb-134">페치할 응용 프로그램의 고유 식별자 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="77fbb-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="77fbb-135">-ObjectId</span></span>
<span data-ttu-id="77fbb-136">반입할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="77fbb-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="77fbb-137">-IncludeTotalCount</span></span>
<span data-ttu-id="77fbb-138">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="77fbb-139">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="77fbb-140">-생략</span><span class="sxs-lookup"><span data-stu-id="77fbb-140">-Skip</span></span>
<span data-ttu-id="77fbb-141">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="77fbb-142">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="77fbb-142">-First</span></span>
<span data-ttu-id="77fbb-143">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="77fbb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fbb-144">CommonParameters</span></span>
<span data-ttu-id="77fbb-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fbb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fbb-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77fbb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fbb-147">입력</span><span class="sxs-lookup"><span data-stu-id="77fbb-147">INPUTS</span></span>

### <span data-ttu-id="77fbb-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77fbb-148">System.String</span></span>

### <span data-ttu-id="77fbb-149">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="77fbb-149">System.Guid</span></span>

## <span data-ttu-id="77fbb-150">출력</span><span class="sxs-lookup"><span data-stu-id="77fbb-150">OUTPUTS</span></span>

### <span data-ttu-id="77fbb-151">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="77fbb-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="77fbb-152">상속자</span><span class="sxs-lookup"><span data-stu-id="77fbb-152">NOTES</span></span>

## <span data-ttu-id="77fbb-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77fbb-153">RELATED LINKS</span></span>

[<span data-ttu-id="77fbb-154">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="77fbb-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="77fbb-155">새로운 AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="77fbb-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="77fbb-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="77fbb-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="77fbb-157">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="77fbb-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="77fbb-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="77fbb-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="77fbb-159">새로운 AzADApplication</span><span class="sxs-lookup"><span data-stu-id="77fbb-159">New-AzADApplication</span></span>](./New-AzADApplication.md)
