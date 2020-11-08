---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046427"
---
# <span data-ttu-id="c4a8c-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="c4a8c-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="c4a8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a8c-102">SYNOPSIS</span></span>

<span data-ttu-id="c4a8c-103">연결에 대 한 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="c4a8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4a8c-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4a8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4a8c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c4a8c-106">**Set-AzureAutomationConnectionFieldValue** Cmdlet은 Azure Automation의 연결에 대 한 필드 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="c4a8c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4a8c-107">EXAMPLES</span></span>

## <span data-ttu-id="c4a8c-108">변수</span><span class="sxs-lookup"><span data-stu-id="c4a8c-108">PARAMETERS</span></span>

### <span data-ttu-id="c4a8c-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4a8c-109">-AutomationAccountName</span></span>
<span data-ttu-id="c4a8c-110">연결을 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-110">Specifies the name of the Automation account with the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a8c-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="c4a8c-111">-ConnectionFieldName</span></span>
<span data-ttu-id="c4a8c-112">필드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-112">Specifies a name for the field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a8c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c4a8c-113">-Name</span></span>
<span data-ttu-id="c4a8c-114">연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-114">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a8c-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="c4a8c-115">-Profile</span></span>
<span data-ttu-id="c4a8c-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4a8c-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a8c-118">-값</span><span class="sxs-lookup"><span data-stu-id="c4a8c-118">-Value</span></span>
<span data-ttu-id="c4a8c-119">연결 필드에 저장할 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a8c-120">CommonParameters</span></span>
<span data-ttu-id="c4a8c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a8c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a8c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a8c-123">입력</span><span class="sxs-lookup"><span data-stu-id="c4a8c-123">INPUTS</span></span>

## <span data-ttu-id="c4a8c-124">출력</span><span class="sxs-lookup"><span data-stu-id="c4a8c-124">OUTPUTS</span></span>

## <span data-ttu-id="c4a8c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="c4a8c-125">NOTES</span></span>

## <span data-ttu-id="c4a8c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4a8c-126">RELATED LINKS</span></span>

[<span data-ttu-id="c4a8c-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c4a8c-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="c4a8c-128">새-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c4a8c-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="c4a8c-129">-AzureAutomationConnection 제거</span><span class="sxs-lookup"><span data-stu-id="c4a8c-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


