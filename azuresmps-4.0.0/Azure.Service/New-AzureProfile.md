---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046000"
---
# <span data-ttu-id="21ba0-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="21ba0-101">New-AzureProfile</span></span>

## <span data-ttu-id="21ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ba0-102">SYNOPSIS</span></span>

## <span data-ttu-id="21ba0-103">구문과</span><span class="sxs-lookup"><span data-stu-id="21ba0-103">SYNTAX</span></span>

### <span data-ttu-id="21ba0-104">인증</span><span class="sxs-lookup"><span data-stu-id="21ba0-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="21ba0-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21ba0-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="21ba0-106">토큰</span><span class="sxs-lookup"><span data-stu-id="21ba0-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="21ba0-107">증명과</span><span class="sxs-lookup"><span data-stu-id="21ba0-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="21ba0-108">비울</span><span class="sxs-lookup"><span data-stu-id="21ba0-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="21ba0-109">파일</span><span class="sxs-lookup"><span data-stu-id="21ba0-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="21ba0-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="21ba0-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="21ba0-111">설명은</span><span class="sxs-lookup"><span data-stu-id="21ba0-111">DESCRIPTION</span></span>

## <span data-ttu-id="21ba0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="21ba0-112">EXAMPLES</span></span>

### <span data-ttu-id="21ba0-113">raid-1</span><span class="sxs-lookup"><span data-stu-id="21ba0-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="21ba0-114">변수</span><span class="sxs-lookup"><span data-stu-id="21ba0-114">PARAMETERS</span></span>

### <span data-ttu-id="21ba0-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="21ba0-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="21ba0-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-117">-인증서</span><span class="sxs-lookup"><span data-stu-id="21ba0-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="21ba0-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-119">-환경</span><span class="sxs-lookup"><span data-stu-id="21ba0-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-120">-Path</span><span class="sxs-lookup"><span data-stu-id="21ba0-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-121">-속성</span><span class="sxs-lookup"><span data-stu-id="21ba0-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21ba0-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="21ba0-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21ba0-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-125">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="21ba0-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ba0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ba0-126">CommonParameters</span></span>
<span data-ttu-id="21ba0-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ba0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ba0-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ba0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ba0-129">입력</span><span class="sxs-lookup"><span data-stu-id="21ba0-129">INPUTS</span></span>

## <span data-ttu-id="21ba0-130">출력</span><span class="sxs-lookup"><span data-stu-id="21ba0-130">OUTPUTS</span></span>

## <span data-ttu-id="21ba0-131">상속자</span><span class="sxs-lookup"><span data-stu-id="21ba0-131">NOTES</span></span>

## <span data-ttu-id="21ba0-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21ba0-132">RELATED LINKS</span></span>

