---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 4ef306b80aaf5fbb03b5ee4e98104829d8853ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702907"
---
# <span data-ttu-id="8808c-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="8808c-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="8808c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8808c-102">SYNOPSIS</span></span>
<span data-ttu-id="8808c-103">자격 증명 모음에서 SCDPM 서버 또는 백업 서버의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8808c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8808c-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8808c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8808c-105">DESCRIPTION</span></span>
<span data-ttu-id="8808c-106">AzureRmRecoveryServicesBackupManagementServer cmdlet은 System Center SCDPM (Data Protection Manager) server 또는 자격 증명 모음에서 Azure Backup server의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="8808c-107">이 cmdlet은 자격 증명 모음에서 등록 취소 된 서버에 대 한 참조를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="8808c-108">컨테이너의 등록을 취소 하려면 먼저 해당 컨테이너와 연결 된 보호 된 데이터를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="8808c-109">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8808c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8808c-110">EXAMPLES</span></span>

### <span data-ttu-id="8808c-111">예제 1: 자격 증명 모음에서 SCDPM 서버 등록 취소</span><span class="sxs-lookup"><span data-stu-id="8808c-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="8808c-112">첫 번째 명령은 dpmserver01.contoso.com 이라는 백업 관리 서버를 가져온 다음이를 $BMS 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="8808c-113">두 번째 명령은 자격 증명 모음에서 SCDPM 서버 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="8808c-114">변수</span><span class="sxs-lookup"><span data-stu-id="8808c-114">PARAMETERS</span></span>

### <span data-ttu-id="8808c-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="8808c-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="8808c-116">등록을 취소할 SCDPM server 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="8808c-117">**BackupManagementServer** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupManagementServer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8808c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8808c-118">-DefaultProfile</span></span>
<span data-ttu-id="8808c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8808c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8808c-120">-PassThru</span></span>
<span data-ttu-id="8808c-121">삭제할 백업 관리 서버를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="8808c-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8808c-122">-VaultId</span></span>
<span data-ttu-id="8808c-123">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-123">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8808c-124">-확인</span><span class="sxs-lookup"><span data-stu-id="8808c-124">-Confirm</span></span>
<span data-ttu-id="8808c-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8808c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8808c-126">-WhatIf</span></span>
<span data-ttu-id="8808c-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8808c-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8808c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8808c-129">CommonParameters</span></span>
<span data-ttu-id="8808c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8808c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8808c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8808c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8808c-132">입력</span><span class="sxs-lookup"><span data-stu-id="8808c-132">INPUTS</span></span>

### <span data-ttu-id="8808c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8808c-133">System.String</span></span>
<span data-ttu-id="8808c-134">매개 변수: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8808c-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="8808c-135">출력</span><span class="sxs-lookup"><span data-stu-id="8808c-135">OUTPUTS</span></span>

### <span data-ttu-id="8808c-136">BackupEngineBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="8808c-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="8808c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8808c-137">NOTES</span></span>

## <span data-ttu-id="8808c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8808c-138">RELATED LINKS</span></span>

[<span data-ttu-id="8808c-139">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="8808c-139">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


