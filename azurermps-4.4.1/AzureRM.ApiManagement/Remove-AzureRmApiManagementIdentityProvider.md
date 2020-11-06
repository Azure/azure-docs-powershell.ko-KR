---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528351"
---
# <span data-ttu-id="1a073-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1a073-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="1a073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a073-102">SYNOPSIS</span></span>
<span data-ttu-id="1a073-103">기존 Id 공급자 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a073-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a073-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a073-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a073-105">DESCRIPTION</span></span>
<span data-ttu-id="1a073-106">기존 Id 공급자 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="1a073-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1a073-107">EXAMPLES</span></span>

### <span data-ttu-id="1a073-108">ApiManagement 서비스에서 Facebook id 공급자 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="1a073-109">Facebook Id 공급자 구성과 관련 된 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="1a073-110">변수</span><span class="sxs-lookup"><span data-stu-id="1a073-110">PARAMETERS</span></span>

### <span data-ttu-id="1a073-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1a073-111">-Context</span></span>
<span data-ttu-id="1a073-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1a073-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1a073-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a073-114">-PassThru</span></span>
<span data-ttu-id="1a073-115">이 cmdlet이 작업이 성공한 경우 $True 값을 반환 하거나 다른 방법으로 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="1a073-116">-Type</span><span class="sxs-lookup"><span data-stu-id="1a073-116">-Type</span></span>
<span data-ttu-id="1a073-117">기존 Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="1a073-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a073-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1a073-119">-Confirm</span></span>
<span data-ttu-id="1a073-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a073-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a073-121">-WhatIf</span></span>
<span data-ttu-id="1a073-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a073-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a073-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a073-124">-DefaultProfile</span></span>
<span data-ttu-id="1a073-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a073-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a073-126">CommonParameters</span></span>
<span data-ttu-id="1a073-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a073-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a073-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a073-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a073-129">입력</span><span class="sxs-lookup"><span data-stu-id="1a073-129">INPUTS</span></span>

## <span data-ttu-id="1a073-130">출력</span><span class="sxs-lookup"><span data-stu-id="1a073-130">OUTPUTS</span></span>

### <span data-ttu-id="1a073-131">부울</span><span class="sxs-lookup"><span data-stu-id="1a073-131">bool</span></span>

## <span data-ttu-id="1a073-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1a073-132">NOTES</span></span>

## <span data-ttu-id="1a073-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a073-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a073-134">새로운 AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1a073-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1a073-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1a073-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1a073-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1a073-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

