---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531270"
---
# <span data-ttu-id="8f72f-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8f72f-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="8f72f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f72f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f72f-103">새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f72f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f72f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f72f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f72f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f72f-106">새 백엔드 엔터티를 만들 때 파이프 될 수 있는 새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="8f72f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8f72f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f72f-108">백 엔드 프록시 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="8f72f-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="8f72f-109">백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="8f72f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8f72f-110">PARAMETERS</span></span>

### <span data-ttu-id="8f72f-111">-암호</span><span class="sxs-lookup"><span data-stu-id="8f72f-111">-Password</span></span>
<span data-ttu-id="8f72f-112">백엔드 프록시에 연결 하는 데 사용 되는 프록시 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="8f72f-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f72f-114">-Url</span><span class="sxs-lookup"><span data-stu-id="8f72f-114">-Url</span></span>
<span data-ttu-id="8f72f-115">전화를 백 엔드로 착신 이동할 때 사용할 프록시 서버의 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="8f72f-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f72f-117">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="8f72f-117">-UserName</span></span>
<span data-ttu-id="8f72f-118">백엔드 프록시에 연결 하는 데 사용 되는 프록시 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="8f72f-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f72f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f72f-120">-DefaultProfile</span></span>
<span data-ttu-id="8f72f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f72f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f72f-122">CommonParameters</span></span>
<span data-ttu-id="8f72f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f72f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f72f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f72f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f72f-125">입력</span><span class="sxs-lookup"><span data-stu-id="8f72f-125">INPUTS</span></span>

## <span data-ttu-id="8f72f-126">출력</span><span class="sxs-lookup"><span data-stu-id="8f72f-126">OUTPUTS</span></span>

### <span data-ttu-id="8f72f-127">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8f72f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="8f72f-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8f72f-128">NOTES</span></span>

## <span data-ttu-id="8f72f-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f72f-129">RELATED LINKS</span></span>

[<span data-ttu-id="8f72f-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8f72f-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="8f72f-131">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8f72f-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8f72f-132">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8f72f-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="8f72f-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8f72f-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8f72f-134">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8f72f-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
