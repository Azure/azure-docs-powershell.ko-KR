---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524955"
---
# <span data-ttu-id="1a011-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1a011-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="1a011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a011-102">SYNOPSIS</span></span>
<span data-ttu-id="1a011-103">기존 active directory 사용자를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a011-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a011-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a011-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a011-105">DESCRIPTION</span></span>
<span data-ttu-id="1a011-106">기존 active directory 사용자를 업데이트 합니다 (회사/학교 계정에도 popularly 알려진 조직 id).</span><span class="sxs-lookup"><span data-stu-id="1a011-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="1a011-107">추가 정보: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="1a011-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="1a011-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1a011-108">EXAMPLES</span></span>

### <span data-ttu-id="1a011-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a011-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1a011-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="1a011-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="1a011-111">변수</span><span class="sxs-lookup"><span data-stu-id="1a011-111">PARAMETERS</span></span>

### <span data-ttu-id="1a011-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a011-112">-DefaultProfile</span></span>
<span data-ttu-id="1a011-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1a011-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a011-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1a011-114">-DisplayName</span></span>
<span data-ttu-id="1a011-115">사용자의 주소록에 표시할 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="1a011-116">예-'Alex Wu '</span><span class="sxs-lookup"><span data-stu-id="1a011-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="1a011-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="1a011-117">-EnableAccount</span></span>
<span data-ttu-id="1a011-118">계정을 사용 하도록 설정 하려면 True이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a011-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="1a011-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="1a011-120">암호를 업데이트 하는 경우에만이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="1a011-121">그렇지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="1a011-122">사용자가 다음에 성공한 로그인 (true)에서 암호를 변경 해야 하는 경우에는이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="1a011-123">기본 동작 (false)은 다음 로그인에 대 한 암호를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="1a011-124">-암호</span><span class="sxs-lookup"><span data-stu-id="1a011-124">-Password</span></span>
<span data-ttu-id="1a011-125">사용자의 새 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-125">New password for the user.</span></span>
<span data-ttu-id="1a011-126">테 넌 트의 암호 복잡성 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="1a011-127">강력한 암호를 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a011-128">-Up. Objectid</span><span class="sxs-lookup"><span data-stu-id="1a011-128">-UPNOrObjectId</span></span>
<span data-ttu-id="1a011-129">사용자 계정 이름 (예: ' someuser@contoso.com ') 또는 속성을 업데이트 해야 하는 사용자의 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="1a011-130">-확인</span><span class="sxs-lookup"><span data-stu-id="1a011-130">-Confirm</span></span>
<span data-ttu-id="1a011-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a011-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a011-132">-WhatIf</span></span>
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

### <span data-ttu-id="1a011-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a011-133">CommonParameters</span></span>
<span data-ttu-id="1a011-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a011-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a011-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a011-136">입력</span><span class="sxs-lookup"><span data-stu-id="1a011-136">INPUTS</span></span>

### <span data-ttu-id="1a011-137">않아야</span><span class="sxs-lookup"><span data-stu-id="1a011-137">None</span></span>
<span data-ttu-id="1a011-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a011-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a011-139">출력</span><span class="sxs-lookup"><span data-stu-id="1a011-139">OUTPUTS</span></span>

### <span data-ttu-id="1a011-140">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="1a011-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="1a011-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1a011-141">NOTES</span></span>

## <span data-ttu-id="1a011-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a011-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a011-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1a011-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="1a011-144">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1a011-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="1a011-145">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1a011-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

