---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534711"
---
# <span data-ttu-id="8795e-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8795e-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="8795e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8795e-102">SYNOPSIS</span></span>
<span data-ttu-id="8795e-103">Active directory 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8795e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8795e-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8795e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8795e-105">DESCRIPTION</span></span>
<span data-ttu-id="8795e-106">Active directory 사용자 (회사/학교 계정 popularly 조직 id 라고도 함)를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="8795e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8795e-107">EXAMPLES</span></span>

### <span data-ttu-id="8795e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8795e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8795e-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="8795e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8795e-110">변수</span><span class="sxs-lookup"><span data-stu-id="8795e-110">PARAMETERS</span></span>

### <span data-ttu-id="8795e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8795e-111">-DefaultProfile</span></span>
<span data-ttu-id="8795e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8795e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8795e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8795e-113">-Force</span></span>
<span data-ttu-id="8795e-114">지정 된 경우 사용자 삭제에 대 한 확인을 요청 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="8795e-115">-Up. Objectid</span><span class="sxs-lookup"><span data-stu-id="8795e-115">-UPNOrObjectId</span></span>
<span data-ttu-id="8795e-116">삭제할 사용자의 사용자 계정 이름 또는 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-116">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="8795e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="8795e-117">-Confirm</span></span>
<span data-ttu-id="8795e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8795e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8795e-119">-WhatIf</span></span>
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

### <span data-ttu-id="8795e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8795e-120">CommonParameters</span></span>
<span data-ttu-id="8795e-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8795e-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8795e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8795e-123">입력</span><span class="sxs-lookup"><span data-stu-id="8795e-123">INPUTS</span></span>

### <span data-ttu-id="8795e-124">않아야</span><span class="sxs-lookup"><span data-stu-id="8795e-124">None</span></span>
<span data-ttu-id="8795e-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8795e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8795e-126">출력</span><span class="sxs-lookup"><span data-stu-id="8795e-126">OUTPUTS</span></span>

## <span data-ttu-id="8795e-127">상속자</span><span class="sxs-lookup"><span data-stu-id="8795e-127">NOTES</span></span>

## <span data-ttu-id="8795e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8795e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8795e-129">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8795e-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="8795e-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8795e-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="8795e-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8795e-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

