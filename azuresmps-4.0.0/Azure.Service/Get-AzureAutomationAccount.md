---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046371"
---
# <span data-ttu-id="1bae9-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1bae9-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="1bae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bae9-102">SYNOPSIS</span></span>

<span data-ttu-id="1bae9-103">Azure Automation 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="1bae9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bae9-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bae9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1bae9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1bae9-106">**Get-AzureAutomationAccount** cmdlet은 구독에 대 한 Microsoft Azure Automation 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="1bae9-107">Automation 계정은 다른 자동화 계정의 리소스에서 격리 된 자동화 리소스에 대 한 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="1bae9-108">자동화 리소스에는 runbook, 작업, 자산 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="1bae9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1bae9-109">EXAMPLES</span></span>

### <span data-ttu-id="1bae9-110">예제 1: Automation 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="1bae9-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="1bae9-111">이 명령은 Contoso17 이라는 자동화 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1bae9-112">변수</span><span class="sxs-lookup"><span data-stu-id="1bae9-112">PARAMETERS</span></span>

### <span data-ttu-id="1bae9-113">-위치</span><span class="sxs-lookup"><span data-stu-id="1bae9-113">-Location</span></span>
<span data-ttu-id="1bae9-114">자동화 계정과 연결 된 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-114">Specifies an Azure location associated with Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bae9-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1bae9-115">-Name</span></span>
<span data-ttu-id="1bae9-116">Azure Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bae9-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="1bae9-117">-Profile</span></span>
<span data-ttu-id="1bae9-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bae9-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bae9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bae9-120">CommonParameters</span></span>
<span data-ttu-id="1bae9-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bae9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bae9-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bae9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bae9-123">입력</span><span class="sxs-lookup"><span data-stu-id="1bae9-123">INPUTS</span></span>

## <span data-ttu-id="1bae9-124">출력</span><span class="sxs-lookup"><span data-stu-id="1bae9-124">OUTPUTS</span></span>

### <span data-ttu-id="1bae9-125">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="1bae9-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="1bae9-126">상속자</span><span class="sxs-lookup"><span data-stu-id="1bae9-126">NOTES</span></span>

## <span data-ttu-id="1bae9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bae9-127">RELATED LINKS</span></span>

[<span data-ttu-id="1bae9-128">새-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1bae9-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="1bae9-129">-AzureAutomationAccount 제거</span><span class="sxs-lookup"><span data-stu-id="1bae9-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


