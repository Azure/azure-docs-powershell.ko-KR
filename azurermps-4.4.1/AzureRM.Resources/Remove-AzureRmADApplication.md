---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532951"
---
# <span data-ttu-id="59d82-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="59d82-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="59d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d82-102">SYNOPSIS</span></span>
<span data-ttu-id="59d82-103">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59d82-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d82-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59d82-105">DESCRIPTION</span></span>
<span data-ttu-id="59d82-106">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="59d82-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59d82-107">EXAMPLES</span></span>

### <span data-ttu-id="59d82-108">--------------------------AAD 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="59d82-109">Azure active directory 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="59d82-110">변수</span><span class="sxs-lookup"><span data-stu-id="59d82-110">PARAMETERS</span></span>

### <span data-ttu-id="59d82-111">-Force</span><span class="sxs-lookup"><span data-stu-id="59d82-111">-Force</span></span>
<span data-ttu-id="59d82-112">확인 없이 응용 프로그램 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-112">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d82-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="59d82-113">-ObjectId</span></span>
<span data-ttu-id="59d82-114">삭제할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d82-115">-확인</span><span class="sxs-lookup"><span data-stu-id="59d82-115">-Confirm</span></span>
<span data-ttu-id="59d82-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d82-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d82-117">-WhatIf</span></span>
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

### <span data-ttu-id="59d82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d82-118">-DefaultProfile</span></span>
<span data-ttu-id="59d82-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d82-120">CommonParameters</span></span>
<span data-ttu-id="59d82-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d82-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d82-123">입력</span><span class="sxs-lookup"><span data-stu-id="59d82-123">INPUTS</span></span>

## <span data-ttu-id="59d82-124">출력</span><span class="sxs-lookup"><span data-stu-id="59d82-124">OUTPUTS</span></span>

## <span data-ttu-id="59d82-125">상속자</span><span class="sxs-lookup"><span data-stu-id="59d82-125">NOTES</span></span>
<span data-ttu-id="59d82-126">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="59d82-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="59d82-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59d82-127">RELATED LINKS</span></span>

[<span data-ttu-id="59d82-128">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="59d82-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="59d82-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="59d82-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="59d82-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="59d82-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="59d82-131">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="59d82-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

