---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 883c4a9892f4525b15369dbb1c3ed6134eb29f00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528646"
---
# <span data-ttu-id="4b7cc-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4b7cc-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="4b7cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7cc-103">백업 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b7cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b7cc-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b7cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b7cc-105">DESCRIPTION</span></span>
<span data-ttu-id="4b7cc-106">**AzureRmBackupVault** Cmdlet은 Azure Backup 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>
<span data-ttu-id="4b7cc-107">백업 자격 증명 모음을 삭제 하려면 먼저 비어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="4b7cc-108">**AzureRmBackupContainer** cmdlet을 사용 하 여 자격 증명 모음에서 IaaS (인프라의 서비스) 가상 컴퓨터 백업 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="4b7cc-109">**RegisteredServer** cmdlet을 사용 하 여 등록 된 다른 서버와 백업 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="4b7cc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4b7cc-110">EXAMPLES</span></span>

### <span data-ttu-id="4b7cc-111">예제 1: Azure 백업 자격 증명 모음 삭제</span><span class="sxs-lookup"><span data-stu-id="4b7cc-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="4b7cc-112">이 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 라는 Azure 백업 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4b7cc-113">이 명령은 파이프라인 연산자를 사용 하 여 해당 자격 증명 모음을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b7cc-114">현재 cmdlet은 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="4b7cc-115">변수</span><span class="sxs-lookup"><span data-stu-id="4b7cc-115">PARAMETERS</span></span>

### <span data-ttu-id="4b7cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7cc-116">-DefaultProfile</span></span>
<span data-ttu-id="4b7cc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b7cc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b7cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4b7cc-118">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7cc-119">-저장실</span><span class="sxs-lookup"><span data-stu-id="4b7cc-119">-Vault</span></span>
<span data-ttu-id="4b7cc-120">이 cmdlet이 제거 하는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="4b7cc-121">**AzureRmBackupVault** 을 얻으려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b7cc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="4b7cc-122">-Confirm</span></span>
<span data-ttu-id="4b7cc-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7cc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b7cc-124">-WhatIf</span></span>
<span data-ttu-id="4b7cc-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b7cc-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7cc-127">CommonParameters</span></span>
<span data-ttu-id="4b7cc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7cc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b7cc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7cc-130">입력</span><span class="sxs-lookup"><span data-stu-id="4b7cc-130">INPUTS</span></span>

### <span data-ttu-id="4b7cc-131">AzureRMBackupVault를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="4b7cc-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="4b7cc-132">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b7cc-132">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="4b7cc-133">출력</span><span class="sxs-lookup"><span data-stu-id="4b7cc-133">OUTPUTS</span></span>

### <span data-ttu-id="4b7cc-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4b7cc-134">System.Void</span></span>

## <span data-ttu-id="4b7cc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4b7cc-135">NOTES</span></span>
* <span data-ttu-id="4b7cc-136">않아야</span><span class="sxs-lookup"><span data-stu-id="4b7cc-136">None</span></span>

## <span data-ttu-id="4b7cc-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b7cc-137">RELATED LINKS</span></span>

[<span data-ttu-id="4b7cc-138">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4b7cc-138">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4b7cc-139">새로운 AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4b7cc-139">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="4b7cc-140">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4b7cc-140">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


