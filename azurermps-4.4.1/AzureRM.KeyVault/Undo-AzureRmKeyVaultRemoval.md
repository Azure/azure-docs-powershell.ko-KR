---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703721"
---
# <span data-ttu-id="c51f6-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="c51f6-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="c51f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c51f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c51f6-103">삭제 된 키 자격 증명 모음을 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c51f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c51f6-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c51f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c51f6-105">DESCRIPTION</span></span>
<span data-ttu-id="c51f6-106">**AzureRmKeyVaultRemoval** cmdlet은 이전에 삭제 된 키 자격 증명 모음을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="c51f6-107">복구 후 복구 된 자격 증명 모음이 활성 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="c51f6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c51f6-108">EXAMPLES</span></span>

### <span data-ttu-id="c51f6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c51f6-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="c51f6-110">이 명령은 eastus2 지역 및 ' MyResourceGroup ' 리소스 그룹에서 이전에 삭제 된 키 자격 증명 모음 ' MyKeyVault '을 활성 및 사용 가능한 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="c51f6-111">또한 태그를 새 태그로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="c51f6-112">변수</span><span class="sxs-lookup"><span data-stu-id="c51f6-112">PARAMETERS</span></span>

### <span data-ttu-id="c51f6-113">-위치</span><span class="sxs-lookup"><span data-stu-id="c51f6-113">-Location</span></span>
<span data-ttu-id="c51f6-114">삭제 된 자격 증명 모음 원본 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51f6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c51f6-115">-ResourceGroupName</span></span>
<span data-ttu-id="c51f6-116">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51f6-117">태그</span><span class="sxs-lookup"><span data-stu-id="c51f6-117">-Tag</span></span>
<span data-ttu-id="c51f6-118">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c51f6-119">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c51f6-119">For example:</span></span>

<span data-ttu-id="c51f6-120">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c51f6-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51f6-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c51f6-121">-VaultName</span></span>
<span data-ttu-id="c51f6-122">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="c51f6-122">Vault name.</span></span>
<span data-ttu-id="c51f6-123">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c51f6-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c51f6-124">-Confirm</span></span>
<span data-ttu-id="c51f6-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c51f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c51f6-126">-WhatIf</span></span>
<span data-ttu-id="c51f6-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c51f6-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c51f6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51f6-129">-DefaultProfile</span></span>
<span data-ttu-id="c51f6-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c51f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51f6-131">CommonParameters</span></span>
<span data-ttu-id="c51f6-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c51f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51f6-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c51f6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51f6-134">입력</span><span class="sxs-lookup"><span data-stu-id="c51f6-134">INPUTS</span></span>

### <span data-ttu-id="c51f6-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c51f6-135">System.String</span></span>
<span data-ttu-id="c51f6-136">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="c51f6-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c51f6-137">출력</span><span class="sxs-lookup"><span data-stu-id="c51f6-137">OUTPUTS</span></span>

### <span data-ttu-id="c51f6-138">Microsoft. KeyVault. PSVault</span><span class="sxs-lookup"><span data-stu-id="c51f6-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="c51f6-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c51f6-139">NOTES</span></span>

## <span data-ttu-id="c51f6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c51f6-140">RELATED LINKS</span></span>

[<span data-ttu-id="c51f6-141">제거-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c51f6-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="c51f6-142">새로운 AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c51f6-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="c51f6-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="c51f6-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
