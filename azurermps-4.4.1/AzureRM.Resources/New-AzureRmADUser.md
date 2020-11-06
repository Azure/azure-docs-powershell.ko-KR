---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536987"
---
# <span data-ttu-id="5d31d-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5d31d-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="5d31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d31d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d31d-103">새 active directory 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d31d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d31d-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d31d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d31d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d31d-106">새 active directory 사용자 (회사/학교 계정 popularly 조직 id 라고도 함)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="5d31d-107">추가 정보: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="5d31d-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="5d31d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5d31d-108">EXAMPLES</span></span>

### <span data-ttu-id="5d31d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d31d-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5d31d-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="5d31d-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="5d31d-111">변수</span><span class="sxs-lookup"><span data-stu-id="5d31d-111">PARAMETERS</span></span>

### <span data-ttu-id="5d31d-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d31d-112">-DisplayName</span></span>
<span data-ttu-id="5d31d-113">사용자의 주소록에 표시할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="5d31d-114">' 정 Wu ' 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="5d31d-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="5d31d-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="5d31d-116">사용자가 다음에 성공한 로그인 (true)에서 암호를 변경 해야 하는 경우에는이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="5d31d-117">기본 동작 (false)은 다음 로그인에 대 한 암호를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="5d31d-118">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="5d31d-118">-ImmutableId</span></span>
<span data-ttu-id="5d31d-119">사용자의 upn (사용자 계정 이름) 속성에 페더레이션 도메인을 사용 하는 경우에만 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d31d-120">-암호</span><span class="sxs-lookup"><span data-stu-id="5d31d-120">-Password</span></span>
<span data-ttu-id="5d31d-121">사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-121">Password for the user.</span></span>
<span data-ttu-id="5d31d-122">테 넌 트의 암호 복잡성 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="5d31d-123">강력한 암호를 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="5d31d-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5d31d-124">-UserPrincipalName</span></span>
<span data-ttu-id="5d31d-125">사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-125">The user principal name.</span></span>
<span data-ttu-id="5d31d-126">예-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="5d31d-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="5d31d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="5d31d-127">-Confirm</span></span>
<span data-ttu-id="5d31d-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d31d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d31d-129">-WhatIf</span></span>
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

### <span data-ttu-id="5d31d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d31d-130">-DefaultProfile</span></span>
<span data-ttu-id="5d31d-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d31d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d31d-132">CommonParameters</span></span>
<span data-ttu-id="5d31d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d31d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d31d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d31d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d31d-135">입력</span><span class="sxs-lookup"><span data-stu-id="5d31d-135">INPUTS</span></span>

## <span data-ttu-id="5d31d-136">출력</span><span class="sxs-lookup"><span data-stu-id="5d31d-136">OUTPUTS</span></span>

### <span data-ttu-id="5d31d-137">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="5d31d-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="5d31d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="5d31d-138">NOTES</span></span>

## <span data-ttu-id="5d31d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d31d-139">RELATED LINKS</span></span>

[<span data-ttu-id="5d31d-140">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5d31d-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="5d31d-141">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5d31d-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="5d31d-142">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5d31d-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
