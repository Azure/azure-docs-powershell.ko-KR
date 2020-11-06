---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528359"
---
# <span data-ttu-id="c90ed-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c90ed-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="c90ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c90ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c90ed-103">백 엔드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c90ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c90ed-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c90ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c90ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c90ed-106">Api Management에서 식별자로 지정 된 백 엔드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="c90ed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c90ed-107">EXAMPLES</span></span>

### <span data-ttu-id="c90ed-108">예제 1: 백엔드 123 제거</span><span class="sxs-lookup"><span data-stu-id="c90ed-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="c90ed-109">변수</span><span class="sxs-lookup"><span data-stu-id="c90ed-109">PARAMETERS</span></span>

### <span data-ttu-id="c90ed-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="c90ed-110">-BackendId</span></span>
<span data-ttu-id="c90ed-111">기존 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-111">Identifier of existing backend.</span></span>
<span data-ttu-id="c90ed-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-112">This parameter is required.</span></span>

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

### <span data-ttu-id="c90ed-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c90ed-113">-Context</span></span>
<span data-ttu-id="c90ed-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c90ed-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c90ed-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c90ed-116">-PassThru</span></span>
<span data-ttu-id="c90ed-117">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c90ed-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-118">This parameter is optional.</span></span>
<span data-ttu-id="c90ed-119">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-119">Default value is false.</span></span>

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

### <span data-ttu-id="c90ed-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c90ed-120">-Confirm</span></span>
<span data-ttu-id="c90ed-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c90ed-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c90ed-122">-WhatIf</span></span>
<span data-ttu-id="c90ed-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c90ed-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c90ed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90ed-125">-DefaultProfile</span></span>
<span data-ttu-id="c90ed-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c90ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90ed-127">CommonParameters</span></span>
<span data-ttu-id="c90ed-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c90ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90ed-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c90ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90ed-130">입력</span><span class="sxs-lookup"><span data-stu-id="c90ed-130">INPUTS</span></span>

## <span data-ttu-id="c90ed-131">출력</span><span class="sxs-lookup"><span data-stu-id="c90ed-131">OUTPUTS</span></span>

### <span data-ttu-id="c90ed-132">부울</span><span class="sxs-lookup"><span data-stu-id="c90ed-132">bool</span></span>

## <span data-ttu-id="c90ed-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c90ed-133">NOTES</span></span>

## <span data-ttu-id="c90ed-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c90ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="c90ed-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c90ed-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="c90ed-136">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c90ed-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="c90ed-137">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c90ed-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="c90ed-138">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c90ed-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="c90ed-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c90ed-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
