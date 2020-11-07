---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: 5f6ff2e89bd3b84a573e02a4584fe69794829453
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702178"
---
# <span data-ttu-id="f7aab-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f7aab-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="f7aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7aab-102">SYNOPSIS</span></span>
<span data-ttu-id="f7aab-103">자동화 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7aab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7aab-104">SYNTAX</span></span>

### <span data-ttu-id="f7aab-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="f7aab-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7aab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f7aab-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7aab-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f7aab-107">DESCRIPTION</span></span>
<span data-ttu-id="f7aab-108">**AzureRmAutomationCredential** cmdlet은 하나 이상의 Azure 자동화 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="f7aab-109">기본적으로 모든 자격 증명이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="f7aab-110">특정 자격 증명을 얻기 위해 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="f7aab-111">보안상의 이유로이 cmdlet은 자격 증명 암호를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="f7aab-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f7aab-112">EXAMPLES</span></span>

### <span data-ttu-id="f7aab-113">예제 1: 모든 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="f7aab-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f7aab-114">이 명령은 Contoso17 이라는 자동화 계정의 모든 자격 증명에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f7aab-115">예제 2: 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="f7aab-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="f7aab-116">이 명령은 Contoso17 이라는 Automation 계정의 ContosoCredential 이라는 자격 증명에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f7aab-117">변수</span><span class="sxs-lookup"><span data-stu-id="f7aab-117">PARAMETERS</span></span>

### <span data-ttu-id="f7aab-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7aab-118">-AutomationAccountName</span></span>
<span data-ttu-id="f7aab-119">이 cmdlet에서 자격 증명을 검색 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7aab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7aab-120">-DefaultProfile</span></span>
<span data-ttu-id="f7aab-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f7aab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7aab-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f7aab-122">-Name</span></span>
<span data-ttu-id="f7aab-123">검색할 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7aab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7aab-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7aab-125">이 cmdlet이 자격 증명을 검색 하는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="f7aab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7aab-126">CommonParameters</span></span>
<span data-ttu-id="f7aab-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7aab-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7aab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7aab-129">입력</span><span class="sxs-lookup"><span data-stu-id="f7aab-129">INPUTS</span></span>

### <span data-ttu-id="f7aab-130">않아야</span><span class="sxs-lookup"><span data-stu-id="f7aab-130">None</span></span>
<span data-ttu-id="f7aab-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7aab-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7aab-132">출력</span><span class="sxs-lookup"><span data-stu-id="f7aab-132">OUTPUTS</span></span>

### <span data-ttu-id="f7aab-133">Microsoft Azure.. m a. 모델-.pst 정보</span><span class="sxs-lookup"><span data-stu-id="f7aab-133">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="f7aab-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f7aab-134">NOTES</span></span>

## <span data-ttu-id="f7aab-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7aab-135">RELATED LINKS</span></span>

[<span data-ttu-id="f7aab-136">새로운 AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f7aab-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="f7aab-137">제거-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f7aab-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="f7aab-138">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f7aab-138">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


