---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046221"
---
# <span data-ttu-id="1ab6b-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ab6b-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="1ab6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ab6b-102">SYNOPSIS</span></span>

<span data-ttu-id="1ab6b-103">자동화에서 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="1ab6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ab6b-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ab6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ab6b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1ab6b-106">**새-AzureAutomationCredential** Cmdlet은 Microsoft Azure Automation에서 자격 증명을 **PSCredential** 개체로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1ab6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1ab6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1ab6b-108">예제 1: 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="1ab6b-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="1ab6b-109">이러한 명령은 MyCredential 이라는 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="1ab6b-110">사용자 이름 및 암호를 포함 하는 자격 증명 개체가 먼저 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="1ab6b-111">그런 다음 마지막 명령에서 자동화 자격 증명을 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="1ab6b-112">변수</span><span class="sxs-lookup"><span data-stu-id="1ab6b-112">PARAMETERS</span></span>

### <span data-ttu-id="1ab6b-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ab6b-113">-AutomationAccountName</span></span>
<span data-ttu-id="1ab6b-114">자격 증명을 저장할 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="1ab6b-115">-설명</span><span class="sxs-lookup"><span data-stu-id="1ab6b-115">-Description</span></span>
<span data-ttu-id="1ab6b-116">자격 증명에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="1ab6b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1ab6b-117">-Name</span></span>
<span data-ttu-id="1ab6b-118">자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="1ab6b-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="1ab6b-119">-Profile</span></span>
<span data-ttu-id="1ab6b-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ab6b-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ab6b-122">-값</span><span class="sxs-lookup"><span data-stu-id="1ab6b-122">-Value</span></span>
<span data-ttu-id="1ab6b-123">자격 증명을 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab6b-124">CommonParameters</span></span>
<span data-ttu-id="1ab6b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ab6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab6b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab6b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab6b-127">입력</span><span class="sxs-lookup"><span data-stu-id="1ab6b-127">INPUTS</span></span>

## <span data-ttu-id="1ab6b-128">출력</span><span class="sxs-lookup"><span data-stu-id="1ab6b-128">OUTPUTS</span></span>

### <span data-ttu-id="1ab6b-129">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="1ab6b-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="1ab6b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1ab6b-130">NOTES</span></span>

## <span data-ttu-id="1ab6b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ab6b-131">RELATED LINKS</span></span>

[<span data-ttu-id="1ab6b-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ab6b-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="1ab6b-133">-AzureAutomationCredential 제거</span><span class="sxs-lookup"><span data-stu-id="1ab6b-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="1ab6b-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ab6b-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


