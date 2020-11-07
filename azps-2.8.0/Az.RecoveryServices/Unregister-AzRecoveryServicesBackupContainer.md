---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 410d78df47a37daa90213056170c86f24c423986
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872586"
---
# <span data-ttu-id="0445b-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0445b-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="0445b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0445b-102">SYNOPSIS</span></span>
<span data-ttu-id="0445b-103">자격 증명 모음에서 Windows Server 또는 다른 컨테이너의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="0445b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0445b-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0445b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0445b-105">DESCRIPTION</span></span>
<span data-ttu-id="0445b-106">AzRecoveryServicesBackupContainer cmdlet은 자격 증명 모음에서 Windows Server 또는 다른 백업 컨테이너의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="0445b-107">이 cmdlet은 자격 증명 모음에서 컨테이너에 대 한 참조를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="0445b-108">컨테이너의 등록을 취소 하려면 먼저 해당 컨테이너와 연결 된 보호 된 데이터를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="0445b-109">현재 cmdlet을 사용 하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0445b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0445b-110">EXAMPLES</span></span>

### <span data-ttu-id="0445b-111">예제 1: 자격 증명 모음에서 Windows Server 등록 취소</span><span class="sxs-lookup"><span data-stu-id="0445b-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="0445b-112">첫 번째 명령은 자격 증명 모음에 등록 되어 있는 server01.contoso.com 이라는 Windows 컨테이너를 가져온 다음이를 $Cont 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="0445b-113">두 번째 명령은 Azure Backup 자격 증명 모음에서 지정 된 Windows Server의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="0445b-114">변수</span><span class="sxs-lookup"><span data-stu-id="0445b-114">PARAMETERS</span></span>

### <span data-ttu-id="0445b-115">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="0445b-115">-Container</span></span>
<span data-ttu-id="0445b-116">등록을 취소할 백업 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="0445b-117">**Backupcontainer** 개체를 가져오려면 Get-AzRecoveryServicesBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0445b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0445b-118">-DefaultProfile</span></span>
<span data-ttu-id="0445b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0445b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0445b-120">-PassThru</span></span>
<span data-ttu-id="0445b-121">삭제할 컨테이너를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="0445b-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0445b-122">-VaultId</span></span>
<span data-ttu-id="0445b-123">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0445b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="0445b-124">-Confirm</span></span>
<span data-ttu-id="0445b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0445b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0445b-126">-WhatIf</span></span>
<span data-ttu-id="0445b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0445b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0445b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0445b-129">CommonParameters</span></span>
<span data-ttu-id="0445b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0445b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0445b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0445b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0445b-132">입력</span><span class="sxs-lookup"><span data-stu-id="0445b-132">INPUTS</span></span>

### <span data-ttu-id="0445b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0445b-133">System.String</span></span>

## <span data-ttu-id="0445b-134">출력</span><span class="sxs-lookup"><span data-stu-id="0445b-134">OUTPUTS</span></span>

### <span data-ttu-id="0445b-135">ContainerBase에서. i. i m/.</span><span class="sxs-lookup"><span data-stu-id="0445b-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="0445b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0445b-136">NOTES</span></span>

## <span data-ttu-id="0445b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0445b-137">RELATED LINKS</span></span>

[<span data-ttu-id="0445b-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0445b-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


