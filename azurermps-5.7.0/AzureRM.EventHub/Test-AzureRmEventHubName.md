---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529827"
---
# <span data-ttu-id="240a6-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="240a6-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="240a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="240a6-102">SYNOPSIS</span></span>
<span data-ttu-id="240a6-103">지정 된 네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="240a6-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="240a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="240a6-104">SYNTAX</span></span>

### <span data-ttu-id="240a6-105">NamespaceCheckNameAvailabilitySet (기본값)</span><span class="sxs-lookup"><span data-stu-id="240a6-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="240a6-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="240a6-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="240a6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="240a6-107">DESCRIPTION</span></span>
<span data-ttu-id="240a6-108">네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 **AzureRmEventhubName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="240a6-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="240a6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="240a6-109">EXAMPLES</span></span>

### <span data-ttu-id="240a6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="240a6-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="240a6-111">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="240a6-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="240a6-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="240a6-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="240a6-113">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 False로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="240a6-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="240a6-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="240a6-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="240a6-115">' MyNameSapceName ' 네임 스페이스에서 별칭 이름 ' myAliasName '의 가용성에 대 한 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="240a6-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="240a6-116">변수</span><span class="sxs-lookup"><span data-stu-id="240a6-116">PARAMETERS</span></span>

### <span data-ttu-id="240a6-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="240a6-117">-AliasName</span></span>
<span data-ttu-id="240a6-118">DR 구성 이름-별칭 이름</span><span class="sxs-lookup"><span data-stu-id="240a6-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240a6-119">-DefaultProfile</span></span>
<span data-ttu-id="240a6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="240a6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240a6-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="240a6-121">-Namespace</span></span>
<span data-ttu-id="240a6-122">Eventhub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="240a6-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="240a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="240a6-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="240a6-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="240a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240a6-125">CommonParameters</span></span>
<span data-ttu-id="240a6-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="240a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="240a6-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240a6-128">입력</span><span class="sxs-lookup"><span data-stu-id="240a6-128">INPUTS</span></span>

### <span data-ttu-id="240a6-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="240a6-129">System.String</span></span>


## <span data-ttu-id="240a6-130">출력</span><span class="sxs-lookup"><span data-stu-id="240a6-130">OUTPUTS</span></span>

### <span data-ttu-id="240a6-131">PSCheckNameAvailabilityResultAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="240a6-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="240a6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="240a6-132">NOTES</span></span>

## <span data-ttu-id="240a6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="240a6-133">RELATED LINKS</span></span>
