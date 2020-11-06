---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537460"
---
# <span data-ttu-id="8811e-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8811e-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="8811e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8811e-102">SYNOPSIS</span></span>
<span data-ttu-id="8811e-103">인지 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8811e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8811e-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8811e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8811e-105">DESCRIPTION</span></span>
<span data-ttu-id="8811e-106">**AzureRmCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8811e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8811e-107">EXAMPLES</span></span>

## <span data-ttu-id="8811e-108">변수</span><span class="sxs-lookup"><span data-stu-id="8811e-108">PARAMETERS</span></span>

### <span data-ttu-id="8811e-109">-Force</span><span class="sxs-lookup"><span data-stu-id="8811e-109">-Force</span></span>
<span data-ttu-id="8811e-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8811e-111">-이름</span><span class="sxs-lookup"><span data-stu-id="8811e-111">-Name</span></span>
<span data-ttu-id="8811e-112">삭제할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-112">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8811e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8811e-113">-ResourceGroupName</span></span>
<span data-ttu-id="8811e-114">인지 서비스 계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="8811e-115">-확인</span><span class="sxs-lookup"><span data-stu-id="8811e-115">-Confirm</span></span>
<span data-ttu-id="8811e-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8811e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8811e-117">-WhatIf</span></span>
<span data-ttu-id="8811e-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8811e-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8811e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8811e-120">-DefaultProfile</span></span>
<span data-ttu-id="8811e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8811e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8811e-122">CommonParameters</span></span>
<span data-ttu-id="8811e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8811e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8811e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8811e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8811e-125">입력</span><span class="sxs-lookup"><span data-stu-id="8811e-125">INPUTS</span></span>

## <span data-ttu-id="8811e-126">출력</span><span class="sxs-lookup"><span data-stu-id="8811e-126">OUTPUTS</span></span>

## <span data-ttu-id="8811e-127">상속자</span><span class="sxs-lookup"><span data-stu-id="8811e-127">NOTES</span></span>

## <span data-ttu-id="8811e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8811e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8811e-129">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8811e-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="8811e-130">새로운 AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8811e-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="8811e-131">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8811e-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


