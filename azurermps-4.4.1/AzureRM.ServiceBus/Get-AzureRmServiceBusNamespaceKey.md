---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530668"
---
# <span data-ttu-id="c6d29-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="c6d29-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="c6d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d29-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d29-103">네임 스페이스에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6d29-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6d29-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6d29-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6d29-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d29-106">**AzureRmServiceBusNamespaceKey** cmdlet은 지정 된 네임 스페이스에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="c6d29-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6d29-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d29-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6d29-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="c6d29-109">지정 된 네임 스페이스에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="c6d29-110">변수</span><span class="sxs-lookup"><span data-stu-id="c6d29-110">PARAMETERS</span></span>

### <span data-ttu-id="c6d29-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6d29-111">-ResourceGroup</span></span>
<span data-ttu-id="c6d29-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d29-113">-DefaultProfile</span></span>
<span data-ttu-id="c6d29-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6d29-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c6d29-115">-Name</span></span>
<span data-ttu-id="c6d29-116">ServiceBus 네임 스페이스 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d29-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6d29-117">-Namespace</span></span>
<span data-ttu-id="c6d29-118">ServiceBus 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d29-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d29-119">CommonParameters</span></span>
<span data-ttu-id="c6d29-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d29-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d29-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d29-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d29-122">입력</span><span class="sxs-lookup"><span data-stu-id="c6d29-122">INPUTS</span></span>

### <span data-ttu-id="c6d29-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6d29-123">-ResourceGroup</span></span>
 <span data-ttu-id="c6d29-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6d29-124">System.String</span></span>
 

### <span data-ttu-id="c6d29-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c6d29-125">-NamespaceName</span></span>
 <span data-ttu-id="c6d29-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6d29-126">System.String</span></span>
 

### <span data-ttu-id="c6d29-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c6d29-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="c6d29-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6d29-128">System.String</span></span>

## <span data-ttu-id="c6d29-129">출력</span><span class="sxs-lookup"><span data-stu-id="c6d29-129">OUTPUTS</span></span>

### <span data-ttu-id="c6d29-130">ServiceBus-. m m g 목록 키</span><span class="sxs-lookup"><span data-stu-id="c6d29-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="c6d29-131">PrimaryConnectionString: 끝점 = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = {SharedAccessKey 값} SecondaryConnectionString: Endpoint = sb://sb-example1.servicebus.windows.net/; SharedAccessKeyName = AuthoRule1 SharedAccessKey = {SharedAccessKey value} PrimaryKey: {PrimaryKey 값} SecondaryKey: {SecondaryKey 값} KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="c6d29-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="c6d29-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c6d29-132">NOTES</span></span>

## <span data-ttu-id="c6d29-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6d29-133">RELATED LINKS</span></span>

