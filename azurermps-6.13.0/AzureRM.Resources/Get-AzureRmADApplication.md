---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530102"
---
# <span data-ttu-id="439b5-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="439b5-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="439b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="439b5-102">SYNOPSIS</span></span>
<span data-ttu-id="439b5-103">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="439b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="439b5-104">SYNTAX</span></span>

### <span data-ttu-id="439b5-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="439b5-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="439b5-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="439b5-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="439b5-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="439b5-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="439b5-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="439b5-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="439b5-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="439b5-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="439b5-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="439b5-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="439b5-111">설명은</span><span class="sxs-lookup"><span data-stu-id="439b5-111">DESCRIPTION</span></span>
<span data-ttu-id="439b5-112">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="439b5-113">Application lookup은 ObjectId, ApplicationId, IdentifierUri 또는 DisplayName으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="439b5-114">매개 변수를 제공 하지 않으면 테 넌 트 아래의 모든 응용 프로그램을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="439b5-115">예제의</span><span class="sxs-lookup"><span data-stu-id="439b5-115">EXAMPLES</span></span>

### <span data-ttu-id="439b5-116">예제 1-모든 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="439b5-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="439b5-117">테 넌 트 아래에 모든 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="439b5-118">예제 2-페이징을 사용 하 여 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="439b5-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="439b5-119">테 넌 트 아래 첫 번째 100 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="439b5-120">예제 3-식별자 URI로 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="439b5-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="439b5-121">식별자 uri를 사용 하는 응용 프로그램을 ""로 가져옵니다 http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="439b5-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="439b5-122">예제 4-개체 id 별 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="439b5-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="439b5-123">개체 id가 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' 인 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="439b5-124">변수</span><span class="sxs-lookup"><span data-stu-id="439b5-124">PARAMETERS</span></span>

### <span data-ttu-id="439b5-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="439b5-125">-ApplicationId</span></span>
<span data-ttu-id="439b5-126">가져올 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="439b5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439b5-127">-DefaultProfile</span></span>
<span data-ttu-id="439b5-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="439b5-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="439b5-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="439b5-129">-DisplayName</span></span>
<span data-ttu-id="439b5-130">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-130">The display name of the application.</span></span>

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

### <span data-ttu-id="439b5-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="439b5-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="439b5-132">표시 이름으로 시작 하는 모든 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="439b5-133">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="439b5-133">-First</span></span>
<span data-ttu-id="439b5-134">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="439b5-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="439b5-135">-IdentifierUri</span></span>
<span data-ttu-id="439b5-136">페치할 응용 프로그램의 고유 식별자 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="439b5-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="439b5-137">-IncludeTotalCount</span></span>
<span data-ttu-id="439b5-138">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="439b5-139">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="439b5-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="439b5-140">-ObjectId</span></span>
<span data-ttu-id="439b5-141">반입할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439b5-142">-생략</span><span class="sxs-lookup"><span data-stu-id="439b5-142">-Skip</span></span>
<span data-ttu-id="439b5-143">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="439b5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439b5-144">CommonParameters</span></span>
<span data-ttu-id="439b5-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="439b5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439b5-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439b5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439b5-147">입력</span><span class="sxs-lookup"><span data-stu-id="439b5-147">INPUTS</span></span>

### <span data-ttu-id="439b5-148">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="439b5-148">System.Guid</span></span>

### <span data-ttu-id="439b5-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="439b5-149">System.String</span></span>

## <span data-ttu-id="439b5-150">출력</span><span class="sxs-lookup"><span data-stu-id="439b5-150">OUTPUTS</span></span>

### <span data-ttu-id="439b5-151">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="439b5-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="439b5-152">상속자</span><span class="sxs-lookup"><span data-stu-id="439b5-152">NOTES</span></span>

## <span data-ttu-id="439b5-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="439b5-153">RELATED LINKS</span></span>

[<span data-ttu-id="439b5-154">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="439b5-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="439b5-155">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="439b5-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="439b5-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="439b5-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="439b5-157">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="439b5-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="439b5-158">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="439b5-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="439b5-159">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="439b5-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)
