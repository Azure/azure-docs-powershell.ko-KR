---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525040"
---
# <span data-ttu-id="4eb36-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4eb36-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="4eb36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb36-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb36-103">모든 Azure 자격 증명, 계정 및 구독 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eb36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4eb36-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb36-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4eb36-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb36-106">모든 Azure 자격 증명, 계정 및 구독 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="4eb36-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4eb36-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb36-108">전역 컨텍스트 지우기</span><span class="sxs-lookup"><span data-stu-id="4eb36-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="4eb36-109">모든 powershell 세션에 대 한 계정, 구독 및 자격 증명 정보를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="4eb36-110">변수</span><span class="sxs-lookup"><span data-stu-id="4eb36-110">PARAMETERS</span></span>

### <span data-ttu-id="4eb36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb36-111">-DefaultProfile</span></span>
<span data-ttu-id="4eb36-112">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4eb36-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb36-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4eb36-113">-Force</span></span>
<span data-ttu-id="4eb36-114">메시지를 표시 하지 않고 전역 범위에서 모든 사용자 및 그룹 삭제</span><span class="sxs-lookup"><span data-stu-id="4eb36-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="4eb36-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eb36-115">-PassThru</span></span>
<span data-ttu-id="4eb36-116">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="4eb36-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="4eb36-117">-범위</span><span class="sxs-lookup"><span data-stu-id="4eb36-117">-Scope</span></span>
<span data-ttu-id="4eb36-118">현재 PowerShell 세션 또는 모든 세션에 대해서만 컨텍스트를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb36-119">-확인</span><span class="sxs-lookup"><span data-stu-id="4eb36-119">-Confirm</span></span>
<span data-ttu-id="4eb36-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb36-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb36-121">-WhatIf</span></span>
<span data-ttu-id="4eb36-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb36-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb36-124">CommonParameters</span></span>
<span data-ttu-id="4eb36-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb36-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb36-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb36-127">입력</span><span class="sxs-lookup"><span data-stu-id="4eb36-127">INPUTS</span></span>

### <span data-ttu-id="4eb36-128">않아야</span><span class="sxs-lookup"><span data-stu-id="4eb36-128">None</span></span>

## <span data-ttu-id="4eb36-129">출력</span><span class="sxs-lookup"><span data-stu-id="4eb36-129">OUTPUTS</span></span>

### <span data-ttu-id="4eb36-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4eb36-130">System.Boolean</span></span>
<span data-ttu-id="4eb36-131">컨텍스트가 성공적으로 지워진 경우 True이 고, 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb36-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="4eb36-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4eb36-132">NOTES</span></span>

## <span data-ttu-id="4eb36-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eb36-133">RELATED LINKS</span></span>

