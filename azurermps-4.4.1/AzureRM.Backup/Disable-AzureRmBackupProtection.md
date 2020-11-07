---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: e25cbbeb4f9920e468638bbae2ef8c53ca241fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702232"
---
# <span data-ttu-id="bdbd3-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bdbd3-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="bdbd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbd3-103">보호 된 백업 항목에 대 한 보호를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdbd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdbd3-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdbd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bdbd3-105">DESCRIPTION</span></span>
<span data-ttu-id="bdbd3-106">**AzureRmBackupProtection** Cmdlet은 Azure 백업 보호 항목에 대 한 보호를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="bdbd3-107">이 cmdlet은 항목의 정기 예약 백업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="bdbd3-108">이 cmdlet은 백업 항목에 대 한 기존 복구 지점을 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="bdbd3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bdbd3-109">EXAMPLES</span></span>

## <span data-ttu-id="bdbd3-110">변수</span><span class="sxs-lookup"><span data-stu-id="bdbd3-110">PARAMETERS</span></span>

### <span data-ttu-id="bdbd3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="bdbd3-111">-Force</span></span>
<span data-ttu-id="bdbd3-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bdbd3-113">-항목</span><span class="sxs-lookup"><span data-stu-id="bdbd3-113">-Item</span></span>
<span data-ttu-id="bdbd3-114">이 cmdlet이 보호를 해제 하는 백업 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-114">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="bdbd3-115">**AzureRmBackupItem** 을 얻으려면 Get-AzureRmBackupItem cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-115">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd3-116">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="bdbd3-116">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="bdbd3-117">이 cmdlet이 기존 복구 지점을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-117">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="bdbd3-118">나중에 저장 된 복구 지점을 삭제 하려면이 cmdlet을 다시 실행 하 고이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-118">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="bdbd3-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bdbd3-119">-Confirm</span></span>
<span data-ttu-id="bdbd3-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbd3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbd3-121">-WhatIf</span></span>
<span data-ttu-id="bdbd3-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbd3-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbd3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd3-124">-DefaultProfile</span></span>
<span data-ttu-id="bdbd3-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdbd3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbd3-126">CommonParameters</span></span>
<span data-ttu-id="bdbd3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbd3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbd3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdbd3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbd3-129">입력</span><span class="sxs-lookup"><span data-stu-id="bdbd3-129">INPUTS</span></span>

### <span data-ttu-id="bdbd3-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bdbd3-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="bdbd3-131">출력</span><span class="sxs-lookup"><span data-stu-id="bdbd3-131">OUTPUTS</span></span>

### <span data-ttu-id="bdbd3-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="bdbd3-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="bdbd3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="bdbd3-133">NOTES</span></span>

## <span data-ttu-id="bdbd3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdbd3-134">RELATED LINKS</span></span>

[<span data-ttu-id="bdbd3-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bdbd3-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="bdbd3-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bdbd3-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


