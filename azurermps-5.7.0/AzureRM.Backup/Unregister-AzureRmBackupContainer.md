---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 059db3658f97a28bda8960384aef4300595dca20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711827"
---
# <span data-ttu-id="94112-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="94112-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="94112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94112-102">SYNOPSIS</span></span>
<span data-ttu-id="94112-103">백업 자격 증명 모음에서 컨테이너의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94112-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94112-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94112-105">설명은</span><span class="sxs-lookup"><span data-stu-id="94112-105">DESCRIPTION</span></span>
<span data-ttu-id="94112-106">AzureRmBackupContainer cmdlet은 Azure Backup 자격 증명 모음에서 Windows Server 또는 Azure 가상 컴퓨터의 등록을 **취소** 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="94112-107">이 cmdlet은 백업 자격 증명 모음에서 컨테이너에 대 한 참조를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="94112-108">컨테이너의 등록을 취소 하려면 먼저 해당 컨테이너와 연결 된 보호 된 데이터를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="94112-109">예제의</span><span class="sxs-lookup"><span data-stu-id="94112-109">EXAMPLES</span></span>

### <span data-ttu-id="94112-110">예제 1: Windows Server 등록 취소</span><span class="sxs-lookup"><span data-stu-id="94112-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="94112-111">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94112-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="94112-112">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="94112-113">두 번째 명령은 Get-AzureRmBackupContainer cmdlet을 사용 하 여 $Vault의 자격 증명 모음에서 지정 된 이름을 가진 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94112-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="94112-114">명령이 $Container 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="94112-115">마지막 명령은 Azure Backup 자격 증명 모음에서 지정 된 Windows Server의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="94112-116">예제 2: 확인 하지 않고 Windows Server 등록 취소</span><span class="sxs-lookup"><span data-stu-id="94112-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="94112-117">이 명령은 첫 번째 예제에서와 마찬가지로 지정 된 Windows 서버를 Azure Backup 자격 증명 모음에서 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="94112-118">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="94112-119">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94112-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="94112-120">변수</span><span class="sxs-lookup"><span data-stu-id="94112-120">PARAMETERS</span></span>

### <span data-ttu-id="94112-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="94112-121">-Container</span></span>
<span data-ttu-id="94112-122">이 cmdlet이 등록 취소 하는 Windows Server 또는 Azure 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="94112-123">**AzureRmBackupContainer** 을 얻으려면 Get-AzureRmBackupContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94112-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94112-124">-DefaultProfile</span></span>
<span data-ttu-id="94112-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="94112-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94112-126">-Force</span><span class="sxs-lookup"><span data-stu-id="94112-126">-Force</span></span>
<span data-ttu-id="94112-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="94112-128">이 매개 변수는 Windows 형식의 **Azurebackupcontainer** 개체에만 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94112-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94112-129">-확인</span><span class="sxs-lookup"><span data-stu-id="94112-129">-Confirm</span></span>
<span data-ttu-id="94112-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94112-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94112-131">-WhatIf</span></span>
<span data-ttu-id="94112-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94112-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94112-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94112-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94112-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94112-134">CommonParameters</span></span>
<span data-ttu-id="94112-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94112-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94112-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94112-137">입력</span><span class="sxs-lookup"><span data-stu-id="94112-137">INPUTS</span></span>

### <span data-ttu-id="94112-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="94112-138">AzureBackupContainer</span></span>

## <span data-ttu-id="94112-139">출력</span><span class="sxs-lookup"><span data-stu-id="94112-139">OUTPUTS</span></span>

### <span data-ttu-id="94112-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="94112-140">AzureBackupJob</span></span>
<span data-ttu-id="94112-141">이 cmdlet은 컨테이너 형식이 Windows Server 인 경우 $Null를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94112-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="94112-142">상속자</span><span class="sxs-lookup"><span data-stu-id="94112-142">NOTES</span></span>
* <span data-ttu-id="94112-143">않아야</span><span class="sxs-lookup"><span data-stu-id="94112-143">None</span></span>

## <span data-ttu-id="94112-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94112-144">RELATED LINKS</span></span>

[<span data-ttu-id="94112-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="94112-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="94112-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="94112-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="94112-147">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="94112-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


