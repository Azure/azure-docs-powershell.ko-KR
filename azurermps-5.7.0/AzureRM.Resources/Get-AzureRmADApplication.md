---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533663"
---
# <span data-ttu-id="7cb06-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7cb06-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="7cb06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb06-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb06-103">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cb06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cb06-104">SYNTAX</span></span>

### <span data-ttu-id="7cb06-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7cb06-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb06-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb06-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb06-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb06-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb06-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb06-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cb06-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb06-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cb06-110">설명은</span><span class="sxs-lookup"><span data-stu-id="7cb06-110">DESCRIPTION</span></span>
<span data-ttu-id="7cb06-111">기존 azure active directory 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="7cb06-112">Application lookup은 ObjectId, ApplicationId, IdentifierUri 또는 DisplayName으로 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="7cb06-113">매개 변수를 제공 하지 않으면 테 넌 트 아래의 모든 응용 프로그램을 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="7cb06-114">예제의</span><span class="sxs-lookup"><span data-stu-id="7cb06-114">EXAMPLES</span></span>

### <span data-ttu-id="7cb06-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cb06-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="7cb06-116">테 넌 트 아래에 모든 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="7cb06-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="7cb06-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="7cb06-118">식별자 uri를 사용 하는 응용 프로그램을 ""로 가져옵니다 http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="7cb06-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="7cb06-119">변수</span><span class="sxs-lookup"><span data-stu-id="7cb06-119">PARAMETERS</span></span>

### <span data-ttu-id="7cb06-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7cb06-120">-ApplicationId</span></span>
<span data-ttu-id="7cb06-121">가져올 응용 프로그램의 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb06-122">-DefaultProfile</span></span>
<span data-ttu-id="7cb06-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7cb06-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb06-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="7cb06-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="7cb06-125">표시 이름으로 시작 하는 모든 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb06-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="7cb06-126">-IdentifierUri</span></span>
<span data-ttu-id="7cb06-127">페치할 응용 프로그램의 고유 식별자 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb06-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7cb06-128">-ObjectId</span></span>
<span data-ttu-id="7cb06-129">반입할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb06-130">CommonParameters</span></span>
<span data-ttu-id="7cb06-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb06-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb06-133">입력</span><span class="sxs-lookup"><span data-stu-id="7cb06-133">INPUTS</span></span>

### <span data-ttu-id="7cb06-134">않아야</span><span class="sxs-lookup"><span data-stu-id="7cb06-134">None</span></span>
<span data-ttu-id="7cb06-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7cb06-136">출력</span><span class="sxs-lookup"><span data-stu-id="7cb06-136">OUTPUTS</span></span>

### <span data-ttu-id="7cb06-137">ActiveDirectory에서 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 목록 '을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cb06-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="7cb06-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7cb06-138">NOTES</span></span>

## <span data-ttu-id="7cb06-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cb06-139">RELATED LINKS</span></span>

[<span data-ttu-id="7cb06-140">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7cb06-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="7cb06-141">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7cb06-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7cb06-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7cb06-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="7cb06-143">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7cb06-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="7cb06-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7cb06-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="7cb06-145">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7cb06-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

