---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528965"
---
# <span data-ttu-id="66163-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="66163-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="66163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66163-102">SYNOPSIS</span></span>
<span data-ttu-id="66163-103">알림 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66163-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66163-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66163-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66163-105">DESCRIPTION</span></span>
<span data-ttu-id="66163-106">**제거-AzureRmAlertRule** cmdlet은 경고 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="66163-107">경고 규칙의 이름과이를 할당 받은 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="66163-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66163-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="66163-109">예제의</span><span class="sxs-lookup"><span data-stu-id="66163-109">EXAMPLES</span></span>

### <span data-ttu-id="66163-110">예제 1: 알림 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="66163-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="66163-111">이 명령은 리소스 그룹 기본값-웹-CentralUS에서 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 이라는 경고 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="66163-112">변수</span><span class="sxs-lookup"><span data-stu-id="66163-112">PARAMETERS</span></span>

### <span data-ttu-id="66163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66163-113">-DefaultProfile</span></span>
<span data-ttu-id="66163-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="66163-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66163-115">-이름</span><span class="sxs-lookup"><span data-stu-id="66163-115">-Name</span></span>
<span data-ttu-id="66163-116">제거할 알림 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="66163-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66163-117">-ResourceGroupName</span></span>
<span data-ttu-id="66163-118">경고 규칙에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66163-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66163-119">CommonParameters</span></span>
<span data-ttu-id="66163-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66163-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66163-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66163-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66163-122">입력</span><span class="sxs-lookup"><span data-stu-id="66163-122">INPUTS</span></span>

### <span data-ttu-id="66163-123">않아야</span><span class="sxs-lookup"><span data-stu-id="66163-123">None</span></span>
<span data-ttu-id="66163-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66163-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66163-125">출력</span><span class="sxs-lookup"><span data-stu-id="66163-125">OUTPUTS</span></span>

### <span data-ttu-id="66163-126">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="66163-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="66163-127">상속자</span><span class="sxs-lookup"><span data-stu-id="66163-127">NOTES</span></span>

## <span data-ttu-id="66163-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66163-128">RELATED LINKS</span></span>

[<span data-ttu-id="66163-129">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="66163-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="66163-130">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="66163-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="66163-131">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="66163-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="66163-132">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="66163-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


