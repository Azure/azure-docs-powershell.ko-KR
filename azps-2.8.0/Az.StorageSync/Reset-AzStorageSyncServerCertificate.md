---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 8df9d0b5149ef3b22477be1f2316bf499a3b1c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871998"
---
# <span data-ttu-id="de6c3-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="de6c3-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="de6c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="de6c3-103">문제 해결에만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-103">Use for troubleshooting only.</span></span> <span data-ttu-id="de6c3-104">이 명령은 저장소 동기화 서비스에 대 한 서버 id를 설명 하는 데 사용 되는 저장소 동기화 서버 인증서를 롤백합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="de6c3-105">구문과</span><span class="sxs-lookup"><span data-stu-id="de6c3-105">SYNTAX</span></span>

### <span data-ttu-id="de6c3-106">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="de6c3-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de6c3-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de6c3-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de6c3-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="de6c3-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de6c3-109">설명은</span><span class="sxs-lookup"><span data-stu-id="de6c3-109">DESCRIPTION</span></span>
<span data-ttu-id="de6c3-110">이 명령은 저장소 동기화 서비스에 대 한 서버 id를 설명 하는 데 사용 되는 저장소 동기화 서버 인증서를 롤 포워드 합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="de6c3-111">이는 문제 해결 시나리오에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="de6c3-112">이 명령을 호출할 때 서버 인증서가 바뀌고,이 서버는 키의 공개 부분을 제출 하 여 등록 된 저장소 동기화 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="de6c3-113">새 인증서가 생성 되므로이 인증서의 만료 시간도 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="de6c3-114">만료 된 인증서를 업데이트 하는 데도이 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="de6c3-115">이 문제는 오랜 시간 동안 서버가 오프 라인인 경우에 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="de6c3-116">예제의</span><span class="sxs-lookup"><span data-stu-id="de6c3-116">EXAMPLES</span></span>

### <span data-ttu-id="de6c3-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="de6c3-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="de6c3-118">이 명령은 로컬 서버 인증서를 롤백하고 서버의 새 id에 대 한 해당 저장소 동기화 서비스에 안전한 방식으로 알립니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="de6c3-119">변수</span><span class="sxs-lookup"><span data-stu-id="de6c3-119">PARAMETERS</span></span>

### <span data-ttu-id="de6c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6c3-120">-DefaultProfile</span></span>
<span data-ttu-id="de6c3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de6c3-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="de6c3-122">-ParentObject</span></span>
<span data-ttu-id="de6c3-123">일반적으로 매개 변수를 통해 전달 되는 Storages<c13> Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="de6c3-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="de6c3-124">-ParentResourceId</span></span>
<span data-ttu-id="de6c3-125">Storages<c13> Cservice 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="de6c3-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="de6c3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de6c3-126">-PassThru</span></span>
<span data-ttu-id="de6c3-127">일반 실행에서이 cmdlet은 성공에 대 한 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="de6c3-128">PassThru 매개 변수를 제공 하는 경우 cmdlet은 성공적으로 실행 된 후 파이프라인에 값을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="de6c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="de6c3-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="de6c3-131">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="de6c3-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="de6c3-132">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="de6c3-133">-확인</span><span class="sxs-lookup"><span data-stu-id="de6c3-133">-Confirm</span></span>
<span data-ttu-id="de6c3-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de6c3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6c3-135">-WhatIf</span></span>
<span data-ttu-id="de6c3-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de6c3-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de6c3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6c3-138">CommonParameters</span></span>
<span data-ttu-id="de6c3-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de6c3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6c3-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6c3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6c3-141">입력</span><span class="sxs-lookup"><span data-stu-id="de6c3-141">INPUTS</span></span>

### <span data-ttu-id="de6c3-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="de6c3-142">System.String</span></span>

### <span data-ttu-id="de6c3-143">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="de6c3-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="de6c3-144">출력</span><span class="sxs-lookup"><span data-stu-id="de6c3-144">OUTPUTS</span></span>

### <span data-ttu-id="de6c3-145">System. 개체</span><span class="sxs-lookup"><span data-stu-id="de6c3-145">System.Object</span></span>
## <span data-ttu-id="de6c3-146">상속자</span><span class="sxs-lookup"><span data-stu-id="de6c3-146">NOTES</span></span>

## <span data-ttu-id="de6c3-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de6c3-147">RELATED LINKS</span></span>
