---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703249"
---
# <span data-ttu-id="0130a-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="0130a-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="0130a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0130a-102">SYNOPSIS</span></span>
<span data-ttu-id="0130a-103">현재 컨텍스트에서 기본값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0130a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0130a-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0130a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0130a-105">DESCRIPTION</span></span>
<span data-ttu-id="0130a-106">Set-AzureRmDefault cmdlet은 현재 컨텍스트의 기본값을 추가 하거나 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="0130a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0130a-107">EXAMPLES</span></span>

### <span data-ttu-id="0130a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0130a-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="0130a-109">이 명령은 기본 리소스 그룹을 사용자가 지정한 리소스 그룹으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="0130a-110">변수</span><span class="sxs-lookup"><span data-stu-id="0130a-110">PARAMETERS</span></span>

### <span data-ttu-id="0130a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0130a-111">-DefaultProfile</span></span>
<span data-ttu-id="0130a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0130a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0130a-113">-Force</span></span>
<span data-ttu-id="0130a-114">지정 된 기본값이 없는 경우 새 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0130a-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="0130a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0130a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0130a-116">기본값으로 설정 되는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0130a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="0130a-117">-Confirm</span></span>
<span data-ttu-id="0130a-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0130a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0130a-119">-WhatIf</span></span>
<span data-ttu-id="0130a-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0130a-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0130a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0130a-122">CommonParameters</span></span>
<span data-ttu-id="0130a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0130a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0130a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0130a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0130a-125">입력</span><span class="sxs-lookup"><span data-stu-id="0130a-125">INPUTS</span></span>

### <span data-ttu-id="0130a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0130a-126">System.String</span></span>

## <span data-ttu-id="0130a-127">출력</span><span class="sxs-lookup"><span data-stu-id="0130a-127">OUTPUTS</span></span>

### <span data-ttu-id="0130a-128">Microsoft. Azure. .Resources. 모델.</span><span class="sxs-lookup"><span data-stu-id="0130a-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="0130a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="0130a-129">NOTES</span></span>

## <span data-ttu-id="0130a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0130a-130">RELATED LINKS</span></span>

