---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045659"
---
# <span data-ttu-id="561dd-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="561dd-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="561dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="561dd-102">SYNOPSIS</span></span>

<span data-ttu-id="561dd-103">Azure Automation 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="561dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="561dd-104">SYNTAX</span></span>

### <span data-ttu-id="561dd-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="561dd-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="561dd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="561dd-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="561dd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="561dd-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="561dd-108">**Get-AzureAutomationCredential** cmdlet은 하나 이상의 Microsoft Azure Automation 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="561dd-109">기본적으로 모든 자격 증명이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="561dd-110">특정 자격 증명을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="561dd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="561dd-111">EXAMPLES</span></span>

### <span data-ttu-id="561dd-112">예제 1: 모든 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="561dd-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="561dd-113">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="561dd-114">예제 2: 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="561dd-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="561dd-115">이 명령은 MyCredential 이라는 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="561dd-116">변수</span><span class="sxs-lookup"><span data-stu-id="561dd-116">PARAMETERS</span></span>

### <span data-ttu-id="561dd-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="561dd-117">-AutomationAccountName</span></span>
<span data-ttu-id="561dd-118">검색할 자격 증명이 있는 automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="561dd-119">-이름</span><span class="sxs-lookup"><span data-stu-id="561dd-119">-Name</span></span>
<span data-ttu-id="561dd-120">검색할 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="561dd-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="561dd-121">-Profile</span></span>
<span data-ttu-id="561dd-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="561dd-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="561dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="561dd-124">CommonParameters</span></span>
<span data-ttu-id="561dd-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="561dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="561dd-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="561dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="561dd-127">입력</span><span class="sxs-lookup"><span data-stu-id="561dd-127">INPUTS</span></span>

## <span data-ttu-id="561dd-128">출력</span><span class="sxs-lookup"><span data-stu-id="561dd-128">OUTPUTS</span></span>

### <span data-ttu-id="561dd-129">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="561dd-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="561dd-130">상속자</span><span class="sxs-lookup"><span data-stu-id="561dd-130">NOTES</span></span>

## <span data-ttu-id="561dd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="561dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="561dd-132">새-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="561dd-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="561dd-133">-AzureAutomationCredential 제거</span><span class="sxs-lookup"><span data-stu-id="561dd-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="561dd-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="561dd-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


