---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534075"
---
# <span data-ttu-id="33ca0-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="33ca0-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="33ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="33ca0-103">알림 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33ca0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33ca0-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33ca0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="33ca0-106">**제거-AzureRmAlertRule** cmdlet은 경고 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="33ca0-107">경고 규칙의 이름과이를 할당 받은 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="33ca0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="33ca0-108">EXAMPLES</span></span>

### <span data-ttu-id="33ca0-109">예제 1: 알림 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="33ca0-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="33ca0-110">이 명령은 리소스 그룹 기본값-웹-CentralUS에서 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 이라는 경고 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="33ca0-111">변수</span><span class="sxs-lookup"><span data-stu-id="33ca0-111">PARAMETERS</span></span>

### <span data-ttu-id="33ca0-112">-이름</span><span class="sxs-lookup"><span data-stu-id="33ca0-112">-Name</span></span>
<span data-ttu-id="33ca0-113">제거할 알림 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-113">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ca0-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33ca0-114">-ResourceGroup</span></span>
<span data-ttu-id="33ca0-115">경고 규칙에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-115">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ca0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ca0-116">-DefaultProfile</span></span>
<span data-ttu-id="33ca0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33ca0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ca0-118">CommonParameters</span></span>
<span data-ttu-id="33ca0-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33ca0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ca0-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ca0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ca0-121">입력</span><span class="sxs-lookup"><span data-stu-id="33ca0-121">INPUTS</span></span>

## <span data-ttu-id="33ca0-122">출력</span><span class="sxs-lookup"><span data-stu-id="33ca0-122">OUTPUTS</span></span>

### <span data-ttu-id="33ca0-123">System.webserver. List ' 1 [Microsoft Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="33ca0-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="33ca0-124">상속자</span><span class="sxs-lookup"><span data-stu-id="33ca0-124">NOTES</span></span>

## <span data-ttu-id="33ca0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33ca0-125">RELATED LINKS</span></span>

[<span data-ttu-id="33ca0-126">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="33ca0-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="33ca0-127">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="33ca0-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="33ca0-128">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="33ca0-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="33ca0-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="33ca0-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="33ca0-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="33ca0-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


