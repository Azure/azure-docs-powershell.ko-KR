---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 41ce5ae67bbc3b21b29740cde1503e474ebe9f8a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042139"
---
# <span data-ttu-id="e6a0a-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e6a0a-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="e6a0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a0a-103">API Management 속성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="e6a0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6a0a-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a0a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a0a-106">**AzApiManagementProperty** Cmdlet은 Azure API Management **속성** 을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="e6a0a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6a0a-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a0a-108">예제 1: 속성 제거</span><span class="sxs-lookup"><span data-stu-id="e6a0a-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="e6a0a-109">이 명령은 ID Property11 인 속성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="e6a0a-110">변수</span><span class="sxs-lookup"><span data-stu-id="e6a0a-110">PARAMETERS</span></span>

### <span data-ttu-id="e6a0a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e6a0a-111">-Context</span></span>
<span data-ttu-id="e6a0a-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="e6a0a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a0a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6a0a-115">-PassThru</span></span>
<span data-ttu-id="e6a0a-116">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="e6a0a-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="e6a0a-117">-PropertyId</span></span>
<span data-ttu-id="e6a0a-118">이 cmdlet이 제거 하는 속성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6a0a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e6a0a-119">-Confirm</span></span>
<span data-ttu-id="e6a0a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a0a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a0a-121">-WhatIf</span></span>
<span data-ttu-id="e6a0a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a0a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a0a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a0a-124">CommonParameters</span></span>
<span data-ttu-id="e6a0a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a0a-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6a0a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a0a-127">입력</span><span class="sxs-lookup"><span data-stu-id="e6a0a-127">INPUTS</span></span>

### <span data-ttu-id="e6a0a-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6a0a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6a0a-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6a0a-129">System.String</span></span>

### <span data-ttu-id="e6a0a-130">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6a0a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6a0a-131">출력</span><span class="sxs-lookup"><span data-stu-id="e6a0a-131">OUTPUTS</span></span>

### <span data-ttu-id="e6a0a-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e6a0a-132">System.Boolean</span></span>

## <span data-ttu-id="e6a0a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e6a0a-133">NOTES</span></span>

## <span data-ttu-id="e6a0a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6a0a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6a0a-135">새로운 AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e6a0a-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="e6a0a-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="e6a0a-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


