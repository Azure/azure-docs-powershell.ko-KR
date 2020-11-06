---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 3b29d1b07ab0c11f42f1a7d4d9326ae19f6b79f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535511"
---
# <span data-ttu-id="aec83-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="aec83-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="aec83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec83-102">SYNOPSIS</span></span>
<span data-ttu-id="aec83-103">Automation 계정에 대 한 등록 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aec83-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aec83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aec83-105">DESCRIPTION</span></span>
<span data-ttu-id="aec83-106">**AzureRmAutomationKey** Cmdlet은 Azure Automation 계정에 대 한 등록 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="aec83-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aec83-107">EXAMPLES</span></span>

### <span data-ttu-id="aec83-108">예제 1: 자동화 계정에 대 한 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="aec83-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="aec83-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 AutomationAccount01 이라는 Azure Automation 계정에 대 한 기본 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="aec83-110">변수</span><span class="sxs-lookup"><span data-stu-id="aec83-110">PARAMETERS</span></span>

### <span data-ttu-id="aec83-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aec83-111">-AutomationAccountName</span></span>
<span data-ttu-id="aec83-112">이 cmdlet에서 키를 다시 생성 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="aec83-113">-KeyType</span><span class="sxs-lookup"><span data-stu-id="aec83-113">-KeyType</span></span>
<span data-ttu-id="aec83-114">에이전트 등록 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-114">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="aec83-115">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-115">Valid values are:</span></span> 

- <span data-ttu-id="aec83-116">주요한</span><span class="sxs-lookup"><span data-stu-id="aec83-116">Primary</span></span> 
- <span data-ttu-id="aec83-117">보조</span><span class="sxs-lookup"><span data-stu-id="aec83-117">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec83-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec83-118">-ResourceGroupName</span></span>
<span data-ttu-id="aec83-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="aec83-120">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 자동화 계정에 대 한 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-120">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aec83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec83-121">-DefaultProfile</span></span>
<span data-ttu-id="aec83-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec83-123">CommonParameters</span></span>
<span data-ttu-id="aec83-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec83-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec83-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec83-126">입력</span><span class="sxs-lookup"><span data-stu-id="aec83-126">INPUTS</span></span>

## <span data-ttu-id="aec83-127">출력</span><span class="sxs-lookup"><span data-stu-id="aec83-127">OUTPUTS</span></span>

### <span data-ttu-id="aec83-128">Microsoft Azure. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="aec83-128">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="aec83-129">상속자</span><span class="sxs-lookup"><span data-stu-id="aec83-129">NOTES</span></span>

## <span data-ttu-id="aec83-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aec83-130">RELATED LINKS</span></span>

