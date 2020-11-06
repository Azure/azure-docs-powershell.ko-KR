---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 6ad62049600f1734beabcc1a322086aad1a92348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531690"
---
# <span data-ttu-id="e0709-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e0709-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="e0709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0709-102">SYNOPSIS</span></span>
<span data-ttu-id="e0709-103">자격 증명 모음에서 Windows Server 또는 다른 컨테이너의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0709-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0709-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0709-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0709-105">DESCRIPTION</span></span>
<span data-ttu-id="e0709-106">AzureRmRecoveryServicesBackupContainer cmdlet은 자격 증명 모음에서 Windows Server 또는 다른 백업 컨테이너의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="e0709-107">이 cmdlet은 자격 증명 모음에서 컨테이너에 대 한 참조를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="e0709-108">컨테이너의 등록을 취소 하려면 먼저 해당 컨테이너와 연결 된 보호 된 데이터를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="e0709-109">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e0709-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e0709-110">EXAMPLES</span></span>

### <span data-ttu-id="e0709-111">예제 1: 자격 증명 모음에서 Windows Server 등록 취소</span><span class="sxs-lookup"><span data-stu-id="e0709-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="e0709-112">첫 번째 명령은 자격 증명 모음에 등록 되어 있는 server01.contoso.com 이라는 Windows 컨테이너를 가져온 다음이를 $Cont 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="e0709-113">두 번째 명령은 Azure Backup 자격 증명 모음에서 지정 된 Windows Server의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="e0709-114">변수</span><span class="sxs-lookup"><span data-stu-id="e0709-114">PARAMETERS</span></span>

### <span data-ttu-id="e0709-115">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="e0709-115">-Container</span></span>
<span data-ttu-id="e0709-116">등록을 취소할 백업 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="e0709-117">**Backupcontainer** 개체를 가져오려면 Get-AzureRmRecoveryServicesBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0709-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0709-118">-DefaultProfile</span></span>
<span data-ttu-id="e0709-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0709-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0709-120">-PassThru</span></span>
<span data-ttu-id="e0709-121">삭제할 컨테이너를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="e0709-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e0709-122">-Confirm</span></span>
<span data-ttu-id="e0709-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0709-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0709-124">-WhatIf</span></span>
<span data-ttu-id="e0709-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0709-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0709-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0709-127">CommonParameters</span></span>
<span data-ttu-id="e0709-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0709-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0709-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0709-130">입력</span><span class="sxs-lookup"><span data-stu-id="e0709-130">INPUTS</span></span>

### <span data-ttu-id="e0709-131">않아야</span><span class="sxs-lookup"><span data-stu-id="e0709-131">None</span></span>
<span data-ttu-id="e0709-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0709-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0709-133">출력</span><span class="sxs-lookup"><span data-stu-id="e0709-133">OUTPUTS</span></span>

## <span data-ttu-id="e0709-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e0709-134">NOTES</span></span>

## <span data-ttu-id="e0709-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0709-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0709-136">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e0709-136">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


