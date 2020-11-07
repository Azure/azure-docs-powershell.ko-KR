---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 35b15fab6888a300fcef9f80b05aa034a9f07ce3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698229"
---
# <span data-ttu-id="29cab-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="29cab-101">Select-AzProfile</span></span>

## <span data-ttu-id="29cab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29cab-102">SYNOPSIS</span></span>
<span data-ttu-id="29cab-103">여러 서비스 프로필을 지 원하는 모듈의 경우 지정 된 서비스 프로필에 해당 하는 cmdlet을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="29cab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29cab-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29cab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29cab-105">DESCRIPTION</span></span>
<span data-ttu-id="29cab-106">여러 서비스 프로필을 지 원하는 모듈의 경우 지정 된 서비스 프로필에 해당 하는 cmdlet을 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="29cab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="29cab-107">EXAMPLES</span></span>

### <span data-ttu-id="29cab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="29cab-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="29cab-109">2019 년 3 월의 AzureStack 프로필에 대 한 cmdlet 로드</span><span class="sxs-lookup"><span data-stu-id="29cab-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="29cab-110">변수</span><span class="sxs-lookup"><span data-stu-id="29cab-110">PARAMETERS</span></span>

### <span data-ttu-id="29cab-111">-이름</span><span class="sxs-lookup"><span data-stu-id="29cab-111">-Name</span></span>
<span data-ttu-id="29cab-112">선택할 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29cab-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29cab-113">-PassThru</span></span>
<span data-ttu-id="29cab-114">있는 경우 cmdlet에서 성공적으로 실행 되는 동안 값을 반환 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="29cab-115">-확인</span><span class="sxs-lookup"><span data-stu-id="29cab-115">-Confirm</span></span>
<span data-ttu-id="29cab-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29cab-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29cab-117">-WhatIf</span></span>
<span data-ttu-id="29cab-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29cab-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29cab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cab-120">CommonParameters</span></span>
<span data-ttu-id="29cab-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29cab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cab-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29cab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cab-123">입력</span><span class="sxs-lookup"><span data-stu-id="29cab-123">INPUTS</span></span>

### <span data-ttu-id="29cab-124">않아야</span><span class="sxs-lookup"><span data-stu-id="29cab-124">None</span></span>

## <span data-ttu-id="29cab-125">출력</span><span class="sxs-lookup"><span data-stu-id="29cab-125">OUTPUTS</span></span>

### <span data-ttu-id="29cab-126">System. 개체</span><span class="sxs-lookup"><span data-stu-id="29cab-126">System.Object</span></span>
## <span data-ttu-id="29cab-127">상속자</span><span class="sxs-lookup"><span data-stu-id="29cab-127">NOTES</span></span>

## <span data-ttu-id="29cab-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29cab-128">RELATED LINKS</span></span>
