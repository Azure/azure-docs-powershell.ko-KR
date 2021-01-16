---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 41caebb8b43c7c050aef2dac77daf51eebdaf42a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366542"
---
# <span data-ttu-id="c4132-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="c4132-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="c4132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4132-102">SYNOPSIS</span></span>
<span data-ttu-id="c4132-103">문제 해결에만 사용</span><span class="sxs-lookup"><span data-stu-id="c4132-103">Use for troubleshooting only.</span></span> <span data-ttu-id="c4132-104">이 명령은 저장소 동기화 서비스에 서버 ID를 설명하는 데 사용되는 저장소 동기화 서버 인증서를 롤링합니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="c4132-105">구문</span><span class="sxs-lookup"><span data-stu-id="c4132-105">SYNTAX</span></span>

### <span data-ttu-id="c4132-106">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4132-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4132-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4132-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4132-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4132-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4132-109">설명</span><span class="sxs-lookup"><span data-stu-id="c4132-109">DESCRIPTION</span></span>
<span data-ttu-id="c4132-110">이 명령은 저장소 동기화 서비스에 서버 ID를 설명하는 데 사용되는 저장소 동기화 서버 인증서를 롤링합니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="c4132-111">이 방법은 문제 해결 시나리오에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="c4132-112">이 명령을 호출하면 서버 인증서가 대체되어 키의 공개 부분을 제출하여 이 서버가 등록된 저장소 동기화 서비스도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="c4132-113">새 인증서가 생성되어 이 인증서의 만료 시간도 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="c4132-114">이 명령을 사용하여 만료된 인증서를 업데이트할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="c4132-115">서버가 장시간 오프라인 상태인 경우 이 문제가 발생될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="c4132-116">예제</span><span class="sxs-lookup"><span data-stu-id="c4132-116">EXAMPLES</span></span>

### <span data-ttu-id="c4132-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4132-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="c4132-118">이 명령은 로컬 서버 인증서를 롤링하고 안전한 방식으로 서버의 새 ID에 대한 해당 저장소 동기화 서비스에 알릴 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="c4132-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4132-119">PARAMETERS</span></span>

### <span data-ttu-id="c4132-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4132-120">-DefaultProfile</span></span>
<span data-ttu-id="c4132-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4132-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c4132-122">-ParentObject</span></span>
<span data-ttu-id="c4132-123">StorageSyncService 개체입니다. 일반적으로 매개 변수를 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4132-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c4132-124">-ParentResourceId</span></span>
<span data-ttu-id="c4132-125">StorageSyncService 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c4132-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4132-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4132-126">-PassThru</span></span>
<span data-ttu-id="c4132-127">정상적인 실행에서 이 cmdlet은 성공 시 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="c4132-128">PassThru 매개 변수를 제공하는 경우 cmdlet은 실행에 성공한 후 파이프라인에 값을 쓴다.</span><span class="sxs-lookup"><span data-stu-id="c4132-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="c4132-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4132-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4132-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4132-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c4132-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="c4132-132">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4132-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4132-133">-Confirm</span></span>
<span data-ttu-id="c4132-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4132-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4132-135">-WhatIf</span></span>
<span data-ttu-id="c4132-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4132-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4132-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4132-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4132-138">CommonParameters</span></span>
<span data-ttu-id="c4132-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4132-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4132-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c4132-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4132-141">입력</span><span class="sxs-lookup"><span data-stu-id="c4132-141">INPUTS</span></span>

### <span data-ttu-id="c4132-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c4132-142">System.String</span></span>

### <span data-ttu-id="c4132-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c4132-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c4132-144">출력</span><span class="sxs-lookup"><span data-stu-id="c4132-144">OUTPUTS</span></span>

### <span data-ttu-id="c4132-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="c4132-145">System.Object</span></span>
## <span data-ttu-id="c4132-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4132-146">NOTES</span></span>

## <span data-ttu-id="c4132-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4132-147">RELATED LINKS</span></span>
