---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529726"
---
# <span data-ttu-id="ab6b8-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ab6b8-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="ab6b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6b8-103">새 active directory 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab6b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab6b8-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab6b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ab6b8-106">새 active directory 사용자 (회사/학교 계정 popularly 조직 id 라고도 함)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ab6b8-107">추가 정보: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="ab6b8-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="ab6b8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ab6b8-108">EXAMPLES</span></span>

### <span data-ttu-id="ab6b8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab6b8-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ab6b8-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="ab6b8-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="ab6b8-111">변수</span><span class="sxs-lookup"><span data-stu-id="ab6b8-111">PARAMETERS</span></span>

### <span data-ttu-id="ab6b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6b8-112">-DefaultProfile</span></span>
<span data-ttu-id="ab6b8-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ab6b8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab6b8-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ab6b8-114">-DisplayName</span></span>
<span data-ttu-id="ab6b8-115">사용자의 주소록에 표시할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="ab6b8-116">' 정 Wu ' 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="ab6b8-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ab6b8-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ab6b8-118">사용자가 다음에 성공한 로그인 (true)에서 암호를 변경 해야 하는 경우에는이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ab6b8-119">기본 동작 (false)은 다음 로그인에 대 한 암호를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6b8-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="ab6b8-120">-ImmutableId</span></span>
<span data-ttu-id="ab6b8-121">사용자의 upn (사용자 계정 이름) 속성에 페더레이션 도메인을 사용 하는 경우에만 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="ab6b8-122">-암호</span><span class="sxs-lookup"><span data-stu-id="ab6b8-122">-Password</span></span>
<span data-ttu-id="ab6b8-123">사용자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-123">Password for the user.</span></span>
<span data-ttu-id="ab6b8-124">테 넌 트의 암호 복잡성 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ab6b8-125">강력한 암호를 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6b8-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ab6b8-126">-UserPrincipalName</span></span>
<span data-ttu-id="ab6b8-127">사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-127">The user principal name.</span></span>
<span data-ttu-id="ab6b8-128">예-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-128">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="ab6b8-129">-확인</span><span class="sxs-lookup"><span data-stu-id="ab6b8-129">-Confirm</span></span>
<span data-ttu-id="ab6b8-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab6b8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab6b8-131">-WhatIf</span></span>
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

### <span data-ttu-id="ab6b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6b8-132">CommonParameters</span></span>
<span data-ttu-id="ab6b8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6b8-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab6b8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6b8-135">입력</span><span class="sxs-lookup"><span data-stu-id="ab6b8-135">INPUTS</span></span>

### <span data-ttu-id="ab6b8-136">않아야</span><span class="sxs-lookup"><span data-stu-id="ab6b8-136">None</span></span>
<span data-ttu-id="ab6b8-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6b8-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab6b8-138">출력</span><span class="sxs-lookup"><span data-stu-id="ab6b8-138">OUTPUTS</span></span>

### <span data-ttu-id="ab6b8-139">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="ab6b8-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ab6b8-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ab6b8-140">NOTES</span></span>

## <span data-ttu-id="ab6b8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab6b8-141">RELATED LINKS</span></span>

[<span data-ttu-id="ab6b8-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ab6b8-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="ab6b8-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ab6b8-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="ab6b8-144">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ab6b8-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
