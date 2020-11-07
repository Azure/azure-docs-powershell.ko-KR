---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702195"
---
# <span data-ttu-id="0874a-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0874a-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="0874a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0874a-102">SYNOPSIS</span></span>
<span data-ttu-id="0874a-103">기존 active directory 사용자를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0874a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0874a-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0874a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0874a-105">DESCRIPTION</span></span>
<span data-ttu-id="0874a-106">기존 active directory 사용자를 업데이트 합니다 (회사/학교 계정에도 popularly 알려진 조직 id).</span><span class="sxs-lookup"><span data-stu-id="0874a-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="0874a-107">추가 정보: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="0874a-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="0874a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0874a-108">EXAMPLES</span></span>

### <span data-ttu-id="0874a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0874a-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0874a-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="0874a-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="0874a-111">변수</span><span class="sxs-lookup"><span data-stu-id="0874a-111">PARAMETERS</span></span>

### <span data-ttu-id="0874a-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0874a-112">-DisplayName</span></span>
<span data-ttu-id="0874a-113">사용자의 주소록에 표시할 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="0874a-114">예-'Alex Wu '</span><span class="sxs-lookup"><span data-stu-id="0874a-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="0874a-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="0874a-115">-EnableAccount</span></span>
<span data-ttu-id="0874a-116">계정을 사용 하도록 설정 하려면 True이 고, 그렇지 않으면 false입니다. 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0874a-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="0874a-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="0874a-118">암호를 업데이트 하는 경우에만이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="0874a-119">그렇지 않으면 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="0874a-120">사용자가 다음에 성공한 로그인 (true)에서 암호를 변경 해야 하는 경우에는이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="0874a-121">기본 동작 (false)은 다음 로그인에 대 한 암호를 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="0874a-122">-암호</span><span class="sxs-lookup"><span data-stu-id="0874a-122">-Password</span></span>
<span data-ttu-id="0874a-123">사용자의 새 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-123">New password for the user.</span></span>
<span data-ttu-id="0874a-124">테 넌 트의 암호 복잡성 요구 사항을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="0874a-125">강력한 암호를 설정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="0874a-126">-Up. Objectid</span><span class="sxs-lookup"><span data-stu-id="0874a-126">-UPNOrObjectId</span></span>
<span data-ttu-id="0874a-127">사용자 계정 이름 (예: ' someuser@contoso.com ') 또는 속성을 업데이트 해야 하는 사용자의 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="0874a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0874a-128">-Confirm</span></span>
<span data-ttu-id="0874a-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0874a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0874a-130">-WhatIf</span></span>
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

### <span data-ttu-id="0874a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0874a-131">-DefaultProfile</span></span>
<span data-ttu-id="0874a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0874a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0874a-133">CommonParameters</span></span>
<span data-ttu-id="0874a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0874a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0874a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0874a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0874a-136">입력</span><span class="sxs-lookup"><span data-stu-id="0874a-136">INPUTS</span></span>

## <span data-ttu-id="0874a-137">출력</span><span class="sxs-lookup"><span data-stu-id="0874a-137">OUTPUTS</span></span>

### <span data-ttu-id="0874a-138">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Aduser</span><span class="sxs-lookup"><span data-stu-id="0874a-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="0874a-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0874a-139">NOTES</span></span>

## <span data-ttu-id="0874a-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0874a-140">RELATED LINKS</span></span>

[<span data-ttu-id="0874a-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0874a-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="0874a-142">새로운 AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0874a-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="0874a-143">제거-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0874a-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

