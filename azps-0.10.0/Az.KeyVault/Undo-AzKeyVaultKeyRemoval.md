---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876685"
---
# <span data-ttu-id="a2a76-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a2a76-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="a2a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2a76-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a76-103">키 자격 증명 모음에서 삭제 된 키를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="a2a76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2a76-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2a76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2a76-105">DESCRIPTION</span></span>
<span data-ttu-id="a2a76-106">**AzKeyVaultKeyRemoval** cmdlet은 이전에 삭제 된 키를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="a2a76-107">복구 된 키는 활성화 되며 모든 일반 키 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="a2a76-108">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a2a76-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a2a76-109">EXAMPLES</span></span>

### <span data-ttu-id="a2a76-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2a76-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="a2a76-111">이 명령을 사용 하면 이전에 삭제 된 ' MyKey ' 키가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a2a76-112">변수</span><span class="sxs-lookup"><span data-stu-id="a2a76-112">PARAMETERS</span></span>

### <span data-ttu-id="a2a76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a76-113">-DefaultProfile</span></span>
<span data-ttu-id="a2a76-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2a76-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a76-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a2a76-115">-Name</span></span>
<span data-ttu-id="a2a76-116">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-116">Key name.</span></span>
<span data-ttu-id="a2a76-117">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a76-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a2a76-118">-VaultName</span></span>
<span data-ttu-id="a2a76-119">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="a2a76-119">Vault name.</span></span>
<span data-ttu-id="a2a76-120">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a76-121">-확인</span><span class="sxs-lookup"><span data-stu-id="a2a76-121">-Confirm</span></span>
<span data-ttu-id="a2a76-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2a76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a76-123">-WhatIf</span></span>
<span data-ttu-id="a2a76-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2a76-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2a76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a76-126">CommonParameters</span></span>
<span data-ttu-id="a2a76-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a76-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a76-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a76-129">입력</span><span class="sxs-lookup"><span data-stu-id="a2a76-129">INPUTS</span></span>

### <span data-ttu-id="a2a76-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2a76-130">System.String</span></span>

## <span data-ttu-id="a2a76-131">출력</span><span class="sxs-lookup"><span data-stu-id="a2a76-131">OUTPUTS</span></span>

### <span data-ttu-id="a2a76-132">Microsoft. KeyVault. Keyvault</span><span class="sxs-lookup"><span data-stu-id="a2a76-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="a2a76-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a2a76-133">NOTES</span></span>

## <span data-ttu-id="a2a76-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2a76-134">RELATED LINKS</span></span>

[<span data-ttu-id="a2a76-135">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2a76-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="a2a76-136">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2a76-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="a2a76-137">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2a76-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

