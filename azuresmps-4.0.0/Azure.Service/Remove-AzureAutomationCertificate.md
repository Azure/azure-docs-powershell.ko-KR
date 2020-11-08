---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046493"
---
# <span data-ttu-id="4846c-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4846c-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="4846c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4846c-102">SYNOPSIS</span></span>

<span data-ttu-id="4846c-103">자동화 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="4846c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4846c-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4846c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4846c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4846c-106">**-AzureAutomationAccount** Cmdlet은 Microsoft Azure Automation에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="4846c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4846c-107">EXAMPLES</span></span>

### <span data-ttu-id="4846c-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="4846c-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="4846c-109">이 명령은 Contoso17 이라는 Automation 계정에서 Cert01 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4846c-110">변수</span><span class="sxs-lookup"><span data-stu-id="4846c-110">PARAMETERS</span></span>

### <span data-ttu-id="4846c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4846c-111">-AutomationAccountName</span></span>
<span data-ttu-id="4846c-112">인증서를 사용 하 여 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="4846c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4846c-113">-Force</span></span>
<span data-ttu-id="4846c-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4846c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4846c-115">-Name</span></span>
<span data-ttu-id="4846c-116">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="4846c-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="4846c-117">-Profile</span></span>
<span data-ttu-id="4846c-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4846c-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4846c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4846c-120">CommonParameters</span></span>
<span data-ttu-id="4846c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4846c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4846c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4846c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4846c-123">입력</span><span class="sxs-lookup"><span data-stu-id="4846c-123">INPUTS</span></span>

## <span data-ttu-id="4846c-124">출력</span><span class="sxs-lookup"><span data-stu-id="4846c-124">OUTPUTS</span></span>

## <span data-ttu-id="4846c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="4846c-125">NOTES</span></span>

## <span data-ttu-id="4846c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4846c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4846c-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4846c-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="4846c-128">새-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4846c-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="4846c-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4846c-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


