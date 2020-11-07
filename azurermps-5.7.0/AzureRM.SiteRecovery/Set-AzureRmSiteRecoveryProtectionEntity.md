---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702510"
---
# <span data-ttu-id="f7bc0-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f7bc0-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="f7bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bc0-103">사이트 복구 보호 엔터티의 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7bc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7bc0-104">SYNTAX</span></span>

### <span data-ttu-id="f7bc0-105">DisableDR (기본값)</span><span class="sxs-lookup"><span data-stu-id="f7bc0-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7bc0-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="f7bc0-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7bc0-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f7bc0-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7bc0-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="f7bc0-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7bc0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f7bc0-109">DESCRIPTION</span></span>
<span data-ttu-id="f7bc0-110">**AzureRmSiteRecoveryProtectionEntity** Cmdlet은 Azure Site Recovery 보호 엔터티의 보호를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="f7bc0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f7bc0-111">EXAMPLES</span></span>

## <span data-ttu-id="f7bc0-112">변수</span><span class="sxs-lookup"><span data-stu-id="f7bc0-112">PARAMETERS</span></span>

### <span data-ttu-id="f7bc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bc0-113">-DefaultProfile</span></span>
<span data-ttu-id="f7bc0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7bc0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f7bc0-115">-Force</span></span>
<span data-ttu-id="f7bc0-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7bc0-117">-OS</span><span class="sxs-lookup"><span data-stu-id="f7bc0-117">-OS</span></span>
<span data-ttu-id="f7bc0-118">운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-118">Specifies the operating system type.</span></span>
<span data-ttu-id="f7bc0-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7bc0-120">창을</span><span class="sxs-lookup"><span data-stu-id="f7bc0-120">Windows</span></span>
- <span data-ttu-id="f7bc0-121">Linux</span><span class="sxs-lookup"><span data-stu-id="f7bc0-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="f7bc0-122">-OSDiskName</span></span>
<span data-ttu-id="f7bc0-123">운영 체제를 포함 하는 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-124">-정책</span><span class="sxs-lookup"><span data-stu-id="f7bc0-124">-Policy</span></span>
<span data-ttu-id="f7bc0-125">사이트 복구 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-126">-보호</span><span class="sxs-lookup"><span data-stu-id="f7bc0-126">-Protection</span></span>
<span data-ttu-id="f7bc0-127">보호를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="f7bc0-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7bc0-129">설정할</span><span class="sxs-lookup"><span data-stu-id="f7bc0-129">Enable</span></span>
- <span data-ttu-id="f7bc0-130">설정할</span><span class="sxs-lookup"><span data-stu-id="f7bc0-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f7bc0-131">-ProtectionEntity</span></span>
<span data-ttu-id="f7bc0-132">보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f7bc0-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f7bc0-134">대상 Azure 저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f7bc0-135">-WaitForCompletion</span></span>
<span data-ttu-id="f7bc0-136">명령이 반환 하기 전에 완료 될 때까지 대기 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-136">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="f7bc0-137">-확인</span><span class="sxs-lookup"><span data-stu-id="f7bc0-137">-Confirm</span></span>
<span data-ttu-id="f7bc0-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7bc0-139">-WhatIf</span></span>
<span data-ttu-id="f7bc0-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f7bc0-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7bc0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bc0-142">CommonParameters</span></span>
<span data-ttu-id="f7bc0-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bc0-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7bc0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bc0-145">입력</span><span class="sxs-lookup"><span data-stu-id="f7bc0-145">INPUTS</span></span>

### <span data-ttu-id="f7bc0-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f7bc0-146">ASRProtectionEntity</span></span>
<span data-ttu-id="f7bc0-147">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7bc0-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="f7bc0-148">출력</span><span class="sxs-lookup"><span data-stu-id="f7bc0-148">OUTPUTS</span></span>

### <span data-ttu-id="f7bc0-149">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="f7bc0-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f7bc0-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f7bc0-150">NOTES</span></span>

## <span data-ttu-id="f7bc0-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7bc0-151">RELATED LINKS</span></span>

[<span data-ttu-id="f7bc0-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f7bc0-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
