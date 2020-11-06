---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528798"
---
# <span data-ttu-id="0fb3b-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="0fb3b-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="0fb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb3b-103">지정 된 네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb3b-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fb3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fb3b-104">SYNTAX</span></span>

### <span data-ttu-id="0fb3b-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0fb3b-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fb3b-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0fb3b-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fb3b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0fb3b-107">DESCRIPTION</span></span>
<span data-ttu-id="0fb3b-108">네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 **AzureRmServiceBusName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="0fb3b-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="0fb3b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0fb3b-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb3b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0fb3b-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0fb3b-111">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb3b-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="0fb3b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="0fb3b-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0fb3b-113">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 False로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb3b-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="0fb3b-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="0fb3b-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="0fb3b-115">변수</span><span class="sxs-lookup"><span data-stu-id="0fb3b-115">PARAMETERS</span></span>

### <span data-ttu-id="0fb3b-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="0fb3b-116">-AliasName</span></span>
<span data-ttu-id="0fb3b-117">DR 구성 이름-별칭 이름</span><span class="sxs-lookup"><span data-stu-id="0fb3b-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb3b-118">-DefaultProfile</span></span>
<span data-ttu-id="0fb3b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fb3b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb3b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0fb3b-120">-Namespace</span></span>
<span data-ttu-id="0fb3b-121">Servicebus 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="0fb3b-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0fb3b-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0fb3b-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb3b-124">CommonParameters</span></span>
<span data-ttu-id="0fb3b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fb3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0fb3b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb3b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb3b-127">입력</span><span class="sxs-lookup"><span data-stu-id="0fb3b-127">INPUTS</span></span>

### <span data-ttu-id="0fb3b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0fb3b-128">System.String</span></span>


## <span data-ttu-id="0fb3b-129">출력</span><span class="sxs-lookup"><span data-stu-id="0fb3b-129">OUTPUTS</span></span>

### <span data-ttu-id="0fb3b-130">ServiceBus ' 1 [[Microsoft Azure. PSCheckNameAvailabilityResultAttributes, Microsoft Azure. ServiceBus, Version = 0.5.0.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0fb3b-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="0fb3b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0fb3b-131">NOTES</span></span>

## <span data-ttu-id="0fb3b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fb3b-132">RELATED LINKS</span></span>
