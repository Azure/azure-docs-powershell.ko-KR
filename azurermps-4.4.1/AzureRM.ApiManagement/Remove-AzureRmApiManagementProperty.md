---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: 333ed1cb778a5a366a7ad26d426559399658db1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525771"
---
# <span data-ttu-id="339e7-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="339e7-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="339e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="339e7-102">SYNOPSIS</span></span>
<span data-ttu-id="339e7-103">API Management 속성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="339e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="339e7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="339e7-105">DESCRIPTION</span></span>
<span data-ttu-id="339e7-106">**AzureRmApiManagementProperty** Cmdlet은 Azure API Management **속성** 을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="339e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="339e7-107">EXAMPLES</span></span>

### <span data-ttu-id="339e7-108">예제 1: 속성 제거</span><span class="sxs-lookup"><span data-stu-id="339e7-108">Example 1: Remove a property</span></span>
```
PS C:\>Remove-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="339e7-109">이 명령은 ID Property11 인 속성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="339e7-110">변수</span><span class="sxs-lookup"><span data-stu-id="339e7-110">PARAMETERS</span></span>

### <span data-ttu-id="339e7-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="339e7-111">-Context</span></span>
<span data-ttu-id="339e7-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="339e7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="339e7-113">-PassThru</span></span>
<span data-ttu-id="339e7-114">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-114">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="339e7-115">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="339e7-115">-PropertyId</span></span>
<span data-ttu-id="339e7-116">이 cmdlet이 제거 하는 속성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-116">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="339e7-117">-확인</span><span class="sxs-lookup"><span data-stu-id="339e7-117">-Confirm</span></span>
<span data-ttu-id="339e7-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339e7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339e7-119">-WhatIf</span></span>
<span data-ttu-id="339e7-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339e7-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339e7-122">-DefaultProfile</span></span>
<span data-ttu-id="339e7-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="339e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339e7-124">CommonParameters</span></span>
<span data-ttu-id="339e7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="339e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339e7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339e7-127">입력</span><span class="sxs-lookup"><span data-stu-id="339e7-127">INPUTS</span></span>

## <span data-ttu-id="339e7-128">출력</span><span class="sxs-lookup"><span data-stu-id="339e7-128">OUTPUTS</span></span>

### <span data-ttu-id="339e7-129">부울</span><span class="sxs-lookup"><span data-stu-id="339e7-129">bool</span></span>

## <span data-ttu-id="339e7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="339e7-130">NOTES</span></span>

## <span data-ttu-id="339e7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="339e7-131">RELATED LINKS</span></span>

[<span data-ttu-id="339e7-132">새로운 AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="339e7-132">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="339e7-133">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="339e7-133">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


