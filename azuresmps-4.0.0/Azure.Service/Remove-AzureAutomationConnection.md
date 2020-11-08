---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046492"
---
# <span data-ttu-id="1b7f1-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1b7f1-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="1b7f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b7f1-102">SYNOPSIS</span></span>

<span data-ttu-id="1b7f1-103">자동화에서 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="1b7f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b7f1-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1b7f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1b7f1-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1b7f1-106">**제거-AzureAutomationConnection** Cmdlet은 Microsoft Azure 자동화의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1b7f1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1b7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="1b7f1-108">예제 1: 연결 제거</span><span class="sxs-lookup"><span data-stu-id="1b7f1-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="1b7f1-109">이 명령은 Contoso17 이라는 자동화 계정에서 MyConnection 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1b7f1-110">변수</span><span class="sxs-lookup"><span data-stu-id="1b7f1-110">PARAMETERS</span></span>

### <span data-ttu-id="1b7f1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1b7f1-111">-AutomationAccountName</span></span>
<span data-ttu-id="1b7f1-112">자격 증명을 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="1b7f1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1b7f1-113">-Force</span></span>
<span data-ttu-id="1b7f1-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b7f1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1b7f1-115">-Name</span></span>
<span data-ttu-id="1b7f1-116">연결의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="1b7f1-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="1b7f1-117">-Profile</span></span>
<span data-ttu-id="1b7f1-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b7f1-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b7f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7f1-120">CommonParameters</span></span>
<span data-ttu-id="1b7f1-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b7f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7f1-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b7f1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7f1-123">입력</span><span class="sxs-lookup"><span data-stu-id="1b7f1-123">INPUTS</span></span>

## <span data-ttu-id="1b7f1-124">출력</span><span class="sxs-lookup"><span data-stu-id="1b7f1-124">OUTPUTS</span></span>

## <span data-ttu-id="1b7f1-125">상속자</span><span class="sxs-lookup"><span data-stu-id="1b7f1-125">NOTES</span></span>

## <span data-ttu-id="1b7f1-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b7f1-126">RELATED LINKS</span></span>

[<span data-ttu-id="1b7f1-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1b7f1-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="1b7f1-128">새-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1b7f1-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="1b7f1-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="1b7f1-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


