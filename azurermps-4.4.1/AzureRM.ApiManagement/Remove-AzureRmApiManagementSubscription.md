---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525755"
---
# <span data-ttu-id="fe489-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fe489-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="fe489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe489-102">SYNOPSIS</span></span>
<span data-ttu-id="fe489-103">기존 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe489-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe489-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe489-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe489-105">DESCRIPTION</span></span>
<span data-ttu-id="fe489-106">**제거-AzureRmApiManagementSubscription** cmdlet은 기존 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="fe489-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe489-107">EXAMPLES</span></span>

### <span data-ttu-id="fe489-108">예제 1: 구독 삭제</span><span class="sxs-lookup"><span data-stu-id="fe489-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="fe489-109">이 명령은 기존 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="fe489-110">변수</span><span class="sxs-lookup"><span data-stu-id="fe489-110">PARAMETERS</span></span>

### <span data-ttu-id="fe489-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fe489-111">-Context</span></span>
<span data-ttu-id="fe489-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe489-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe489-113">-PassThru</span></span>
<span data-ttu-id="fe489-114">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $false의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe489-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe489-115">-SubscriptionId</span></span>
<span data-ttu-id="fe489-116">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-116">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="fe489-117">-확인</span><span class="sxs-lookup"><span data-stu-id="fe489-117">-Confirm</span></span>
<span data-ttu-id="fe489-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe489-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe489-119">-WhatIf</span></span>
<span data-ttu-id="fe489-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe489-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe489-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe489-122">-DefaultProfile</span></span>
<span data-ttu-id="fe489-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe489-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe489-124">CommonParameters</span></span>
<span data-ttu-id="fe489-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe489-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe489-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe489-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe489-127">입력</span><span class="sxs-lookup"><span data-stu-id="fe489-127">INPUTS</span></span>

## <span data-ttu-id="fe489-128">출력</span><span class="sxs-lookup"><span data-stu-id="fe489-128">OUTPUTS</span></span>

### <span data-ttu-id="fe489-129">나타내는</span><span class="sxs-lookup"><span data-stu-id="fe489-129">Boolean</span></span>

## <span data-ttu-id="fe489-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fe489-130">NOTES</span></span>

## <span data-ttu-id="fe489-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe489-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe489-132">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fe489-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="fe489-133">새로운 AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fe489-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="fe489-134">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fe489-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


