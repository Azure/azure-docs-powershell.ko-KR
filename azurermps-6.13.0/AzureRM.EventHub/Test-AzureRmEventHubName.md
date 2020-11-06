---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: 64a8282cb1dc99b32e0296ebf97f59ab96b5fd96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524411"
---
# <span data-ttu-id="fd2c2-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="fd2c2-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="fd2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2c2-103">지정 된 네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 사용 가능 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2c2-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd2c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd2c2-104">SYNTAX</span></span>

### <span data-ttu-id="fd2c2-105">NamespaceCheckNameAvailabilitySet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd2c2-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd2c2-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fd2c2-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd2c2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd2c2-107">DESCRIPTION</span></span>
<span data-ttu-id="fd2c2-108">네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 **AzureRmEventhubName** Cmdlet 검사 사용 가능성</span><span class="sxs-lookup"><span data-stu-id="fd2c2-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="fd2c2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fd2c2-109">EXAMPLES</span></span>

### <span data-ttu-id="fd2c2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd2c2-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="fd2c2-111">사용 가능한 경우 네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2c2-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="fd2c2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fd2c2-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="fd2c2-113">네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 False로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2c2-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="fd2c2-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="fd2c2-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="fd2c2-115">사용 가능한 경우 ' MyNameSapceName ' 네임 스페이스에 대 한 별칭 이름 ' myAliasName '의 사용 가능 상태를 True로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2c2-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="fd2c2-116">변수</span><span class="sxs-lookup"><span data-stu-id="fd2c2-116">PARAMETERS</span></span>

### <span data-ttu-id="fd2c2-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fd2c2-117">-AliasName</span></span>
<span data-ttu-id="fd2c2-118">DR 구성 이름-별칭 이름</span><span class="sxs-lookup"><span data-stu-id="fd2c2-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2c2-119">-DefaultProfile</span></span>
<span data-ttu-id="fd2c2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd2c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd2c2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd2c2-121">-Namespace</span></span>
<span data-ttu-id="fd2c2-122">Eventhub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="fd2c2-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="fd2c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd2c2-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fd2c2-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2c2-125">CommonParameters</span></span>
<span data-ttu-id="fd2c2-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd2c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2c2-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd2c2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2c2-128">입력</span><span class="sxs-lookup"><span data-stu-id="fd2c2-128">INPUTS</span></span>

### <span data-ttu-id="fd2c2-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd2c2-129">System.String</span></span>

## <span data-ttu-id="fd2c2-130">출력</span><span class="sxs-lookup"><span data-stu-id="fd2c2-130">OUTPUTS</span></span>

### <span data-ttu-id="fd2c2-131">PSCheckNameAvailabilityResultAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="fd2c2-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="fd2c2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fd2c2-132">NOTES</span></span>

## <span data-ttu-id="fd2c2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd2c2-133">RELATED LINKS</span></span>
