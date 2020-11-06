---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536316"
---
# <span data-ttu-id="07cae-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="07cae-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="07cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07cae-102">SYNOPSIS</span></span>
<span data-ttu-id="07cae-103">키 자격 증명 모음에서 삭제 된 키를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07cae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07cae-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07cae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07cae-105">DESCRIPTION</span></span>
<span data-ttu-id="07cae-106">**AzureKeyVaultKeyRemoval** cmdlet은 이전에 삭제 된 키를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="07cae-107">복구 된 키는 활성화 되며 모든 일반 키 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="07cae-108">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="07cae-109">예제의</span><span class="sxs-lookup"><span data-stu-id="07cae-109">EXAMPLES</span></span>

### <span data-ttu-id="07cae-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="07cae-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="07cae-111">이 명령을 사용 하면 이전에 삭제 된 ' MyKey ' 키가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="07cae-112">변수</span><span class="sxs-lookup"><span data-stu-id="07cae-112">PARAMETERS</span></span>

### <span data-ttu-id="07cae-113">-이름</span><span class="sxs-lookup"><span data-stu-id="07cae-113">-Name</span></span>
<span data-ttu-id="07cae-114">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-114">Key name.</span></span>
<span data-ttu-id="07cae-115">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07cae-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="07cae-116">-VaultName</span></span>
<span data-ttu-id="07cae-117">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="07cae-117">Vault name.</span></span>
<span data-ttu-id="07cae-118">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="07cae-119">-확인</span><span class="sxs-lookup"><span data-stu-id="07cae-119">-Confirm</span></span>
<span data-ttu-id="07cae-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07cae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07cae-121">-WhatIf</span></span>
<span data-ttu-id="07cae-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07cae-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07cae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cae-124">-DefaultProfile</span></span>
<span data-ttu-id="07cae-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07cae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cae-126">CommonParameters</span></span>
<span data-ttu-id="07cae-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07cae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cae-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07cae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cae-129">입력</span><span class="sxs-lookup"><span data-stu-id="07cae-129">INPUTS</span></span>

### <span data-ttu-id="07cae-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07cae-130">System.String</span></span>

## <span data-ttu-id="07cae-131">출력</span><span class="sxs-lookup"><span data-stu-id="07cae-131">OUTPUTS</span></span>

### <span data-ttu-id="07cae-132">Microsoft. KeyVault. Keyvault</span><span class="sxs-lookup"><span data-stu-id="07cae-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="07cae-133">상속자</span><span class="sxs-lookup"><span data-stu-id="07cae-133">NOTES</span></span>

## <span data-ttu-id="07cae-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07cae-134">RELATED LINKS</span></span>

[<span data-ttu-id="07cae-135">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="07cae-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="07cae-136">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="07cae-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="07cae-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="07cae-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

