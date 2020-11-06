---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530505"
---
# <span data-ttu-id="9ad62-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="9ad62-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="9ad62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ad62-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad62-103">IotHub connectionstrings를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ad62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ad62-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ad62-105">DESCRIPTION</span></span>
<span data-ttu-id="9ad62-106">IotHub connectionstrings를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="9ad62-107">모든 키에 대해 connectionstrings를 가져오거나 특정 키 이름으로 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="9ad62-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9ad62-108">EXAMPLES</span></span>

### <span data-ttu-id="9ad62-109">예제 1 모든 IotHub connectionstrings 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ad62-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9ad62-110">"Myiothub" iothub의 모든 키에 대 한 connectionstrings를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="9ad62-111">예제 2 특정 키에 대 한 IotHub connectionstrings 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ad62-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="9ad62-112">"Myiothub" 이라는 iothub에 대 한 "mykey" 키의 connectionstrings를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="9ad62-113">변수</span><span class="sxs-lookup"><span data-stu-id="9ad62-113">PARAMETERS</span></span>

### <span data-ttu-id="9ad62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad62-114">-DefaultProfile</span></span>
<span data-ttu-id="9ad62-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ad62-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ad62-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9ad62-116">-KeyName</span></span>
<span data-ttu-id="9ad62-117">키 이름</span><span class="sxs-lookup"><span data-stu-id="9ad62-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad62-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9ad62-118">-Name</span></span>
<span data-ttu-id="9ad62-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad62-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ad62-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9ad62-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad62-122">CommonParameters</span></span>
<span data-ttu-id="9ad62-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad62-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad62-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad62-125">입력</span><span class="sxs-lookup"><span data-stu-id="9ad62-125">INPUTS</span></span>

### <span data-ttu-id="9ad62-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ad62-126">System.String</span></span>

## <span data-ttu-id="9ad62-127">출력</span><span class="sxs-lookup"><span data-stu-id="9ad62-127">OUTPUTS</span></span>

### <span data-ttu-id="9ad62-128">IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule</span><span class="sxs-lookup"><span data-stu-id="9ad62-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="9ad62-129">System.webserver. \` \[ \[ IotHub는 1. IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = l a n,이에 해당 하는. m a.\]\]</span><span class="sxs-lookup"><span data-stu-id="9ad62-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="9ad62-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9ad62-130">NOTES</span></span>

## <span data-ttu-id="9ad62-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ad62-131">RELATED LINKS</span></span>

