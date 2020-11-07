---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703225"
---
# <span data-ttu-id="e02f9-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e02f9-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="e02f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e02f9-103">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e02f9-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e02f9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e02f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e02f9-106">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="e02f9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e02f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e02f9-108">AAD 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="e02f9-109">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="e02f9-110">변수</span><span class="sxs-lookup"><span data-stu-id="e02f9-110">PARAMETERS</span></span>

### <span data-ttu-id="e02f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02f9-111">-DefaultProfile</span></span>
<span data-ttu-id="e02f9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e02f9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e02f9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e02f9-113">-Force</span></span>
<span data-ttu-id="e02f9-114">확인 없이 응용 프로그램 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-114">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e02f9-115">-ObjectId</span></span>
<span data-ttu-id="e02f9-116">삭제할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-117">-확인</span><span class="sxs-lookup"><span data-stu-id="e02f9-117">-Confirm</span></span>
<span data-ttu-id="e02f9-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02f9-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02f9-120">CommonParameters</span></span>
<span data-ttu-id="e02f9-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02f9-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02f9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02f9-123">입력</span><span class="sxs-lookup"><span data-stu-id="e02f9-123">INPUTS</span></span>

### <span data-ttu-id="e02f9-124">않아야</span><span class="sxs-lookup"><span data-stu-id="e02f9-124">None</span></span>
<span data-ttu-id="e02f9-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e02f9-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e02f9-126">출력</span><span class="sxs-lookup"><span data-stu-id="e02f9-126">OUTPUTS</span></span>

## <span data-ttu-id="e02f9-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e02f9-127">NOTES</span></span>
<span data-ttu-id="e02f9-128">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="e02f9-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e02f9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e02f9-129">RELATED LINKS</span></span>

[<span data-ttu-id="e02f9-130">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e02f9-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="e02f9-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e02f9-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="e02f9-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e02f9-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="e02f9-133">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e02f9-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

