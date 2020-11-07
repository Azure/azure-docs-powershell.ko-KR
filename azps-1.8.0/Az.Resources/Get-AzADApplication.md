---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 18b5f64426b0a3c458ea489d27781f1a01336b52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699461"
---
# <span data-ttu-id="eb577-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="eb577-101">Get-AzADApplication</span></span>

## <span data-ttu-id="eb577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb577-102">SYNOPSIS</span></span>
<span data-ttu-id="eb577-103">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="eb577-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb577-104">SYNTAX</span></span>

### <span data-ttu-id="eb577-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb577-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="eb577-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb577-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="eb577-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb577-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="eb577-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb577-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="eb577-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb577-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="eb577-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb577-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="eb577-111">설명은</span><span class="sxs-lookup"><span data-stu-id="eb577-111">DESCRIPTION</span></span>
<span data-ttu-id="eb577-112">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="eb577-113">Application lookup은 ObjectId, ApplicationId, IdentifierUri 또는 DisplayName으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="eb577-114">매개 변수를 제공 하지 않으면 테 넌 트 아래의 모든 응용 프로그램을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="eb577-115">예제의</span><span class="sxs-lookup"><span data-stu-id="eb577-115">EXAMPLES</span></span>

### <span data-ttu-id="eb577-116">예제 1-모든 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="eb577-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="eb577-117">테 넌 트 아래에 모든 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="eb577-118">예제 2-페이징을 사용 하 여 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="eb577-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="eb577-119">테 넌 트 아래 첫 번째 100 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="eb577-120">예제 3-식별자 URI로 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="eb577-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="eb577-121">식별자 uri를 사용 하는 응용 프로그램을 ""로 가져옵니다 http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="eb577-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="eb577-122">예제 4-개체 id 별 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="eb577-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="eb577-123">개체 id가 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' 인 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="eb577-124">변수</span><span class="sxs-lookup"><span data-stu-id="eb577-124">PARAMETERS</span></span>

### <span data-ttu-id="eb577-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="eb577-125">-ApplicationId</span></span>
<span data-ttu-id="eb577-126">가져올 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="eb577-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb577-127">-DefaultProfile</span></span>
<span data-ttu-id="eb577-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eb577-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb577-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb577-129">-DisplayName</span></span>
<span data-ttu-id="eb577-130">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-130">The display name of the application.</span></span>

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

### <span data-ttu-id="eb577-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="eb577-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="eb577-132">표시 이름으로 시작 하는 모든 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="eb577-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="eb577-133">-IdentifierUri</span></span>
<span data-ttu-id="eb577-134">페치할 응용 프로그램의 고유 식별자 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="eb577-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="eb577-135">-ObjectId</span></span>
<span data-ttu-id="eb577-136">반입할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="eb577-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="eb577-137">-IncludeTotalCount</span></span>
<span data-ttu-id="eb577-138">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="eb577-139">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="eb577-140">-생략</span><span class="sxs-lookup"><span data-stu-id="eb577-140">-Skip</span></span>
<span data-ttu-id="eb577-141">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="eb577-142">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="eb577-142">-First</span></span>
<span data-ttu-id="eb577-143">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="eb577-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb577-144">CommonParameters</span></span>
<span data-ttu-id="eb577-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb577-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb577-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb577-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb577-147">입력</span><span class="sxs-lookup"><span data-stu-id="eb577-147">INPUTS</span></span>

### <span data-ttu-id="eb577-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb577-148">System.String</span></span>

### <span data-ttu-id="eb577-149">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="eb577-149">System.Guid</span></span>

## <span data-ttu-id="eb577-150">출력</span><span class="sxs-lookup"><span data-stu-id="eb577-150">OUTPUTS</span></span>

### <span data-ttu-id="eb577-151">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="eb577-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="eb577-152">상속자</span><span class="sxs-lookup"><span data-stu-id="eb577-152">NOTES</span></span>

## <span data-ttu-id="eb577-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb577-153">RELATED LINKS</span></span>

[<span data-ttu-id="eb577-154">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="eb577-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="eb577-155">새로운 AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="eb577-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="eb577-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="eb577-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="eb577-157">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="eb577-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="eb577-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="eb577-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="eb577-159">새로운 AzADApplication</span><span class="sxs-lookup"><span data-stu-id="eb577-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

