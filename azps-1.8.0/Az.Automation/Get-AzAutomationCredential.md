---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701636"
---
# <span data-ttu-id="4a374-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4a374-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="4a374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a374-102">SYNOPSIS</span></span>
<span data-ttu-id="4a374-103">자동화 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="4a374-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a374-104">SYNTAX</span></span>

### <span data-ttu-id="4a374-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a374-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a374-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4a374-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a374-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4a374-107">DESCRIPTION</span></span>
<span data-ttu-id="4a374-108">**AzAutomationCredential** cmdlet은 하나 이상의 Azure 자동화 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="4a374-109">기본적으로 모든 자격 증명이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="4a374-110">특정 자격 증명을 얻기 위해 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="4a374-111">보안상의 이유로이 cmdlet은 자격 증명 암호를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="4a374-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4a374-112">EXAMPLES</span></span>

### <span data-ttu-id="4a374-113">예제 1: 모든 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a374-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4a374-114">이 명령은 Contoso17 이라는 자동화 계정의 모든 자격 증명에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4a374-115">예제 2: 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a374-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="4a374-116">이 명령은 Contoso17 이라는 Automation 계정의 ContosoCredential 이라는 자격 증명에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4a374-117">변수</span><span class="sxs-lookup"><span data-stu-id="4a374-117">PARAMETERS</span></span>

### <span data-ttu-id="4a374-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a374-118">-AutomationAccountName</span></span>
<span data-ttu-id="4a374-119">이 cmdlet에서 자격 증명을 검색 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a374-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a374-120">-DefaultProfile</span></span>
<span data-ttu-id="4a374-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4a374-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a374-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4a374-122">-Name</span></span>
<span data-ttu-id="4a374-123">검색할 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a374-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a374-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a374-125">이 cmdlet이 자격 증명을 검색 하는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="4a374-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a374-126">CommonParameters</span></span>
<span data-ttu-id="4a374-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a374-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a374-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a374-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a374-129">입력</span><span class="sxs-lookup"><span data-stu-id="4a374-129">INPUTS</span></span>

### <span data-ttu-id="4a374-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a374-130">System.String</span></span>

## <span data-ttu-id="4a374-131">출력</span><span class="sxs-lookup"><span data-stu-id="4a374-131">OUTPUTS</span></span>

### <span data-ttu-id="4a374-132">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="4a374-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="4a374-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4a374-133">NOTES</span></span>

## <span data-ttu-id="4a374-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a374-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a374-135">새로운 AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4a374-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="4a374-136">제거-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4a374-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="4a374-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4a374-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


