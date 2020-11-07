---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: f578fa3aab2cf89dcb8d3a753855ded57eaf35db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703579"
---
# <span data-ttu-id="9d7ba-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d7ba-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="9d7ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7ba-103">백업 자격 증명 모음의 저장소 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d7ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d7ba-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d7ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9d7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7ba-106">**AzureRmBackupVault** Cmdlet은 Azure Backup 자격 증명 모음의 저장소 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="9d7ba-107">저장실의 다른 속성은 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="9d7ba-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9d7ba-108">EXAMPLES</span></span>

### <span data-ttu-id="9d7ba-109">예제 1: 기존 자격 증명 모음의 저장소 변경</span><span class="sxs-lookup"><span data-stu-id="9d7ba-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="9d7ba-110">이 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 라는 Azure 백업 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="9d7ba-111">이 명령은 파이프라인 연산자를 사용 하 여 해당 자격 증명 모음을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9d7ba-112">현재 cmdlet은 저장소 유형을 LocallyRedundant로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="9d7ba-113">변수</span><span class="sxs-lookup"><span data-stu-id="9d7ba-113">PARAMETERS</span></span>

### <span data-ttu-id="9d7ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7ba-114">-DefaultProfile</span></span>
<span data-ttu-id="9d7ba-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d7ba-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d7ba-116">-저장소</span><span class="sxs-lookup"><span data-stu-id="9d7ba-116">-Storage</span></span>
<span data-ttu-id="9d7ba-117">백업 데이터의 저장소 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="9d7ba-118">이 매개 변수에 허용 되는 값은 LocallyRedundant 및 GeoRedundant입니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ba-119">-저장실</span><span class="sxs-lookup"><span data-stu-id="9d7ba-119">-Vault</span></span>
<span data-ttu-id="9d7ba-120">이 cmdlet이 수정 하는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="9d7ba-121">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7ba-122">CommonParameters</span></span>
<span data-ttu-id="9d7ba-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7ba-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7ba-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7ba-125">입력</span><span class="sxs-lookup"><span data-stu-id="9d7ba-125">INPUTS</span></span>

### <span data-ttu-id="9d7ba-126">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d7ba-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="9d7ba-127">출력</span><span class="sxs-lookup"><span data-stu-id="9d7ba-127">OUTPUTS</span></span>

### <span data-ttu-id="9d7ba-128">않아야</span><span class="sxs-lookup"><span data-stu-id="9d7ba-128">None</span></span>

## <span data-ttu-id="9d7ba-129">상속자</span><span class="sxs-lookup"><span data-stu-id="9d7ba-129">NOTES</span></span>
* <span data-ttu-id="9d7ba-130">보관소의 첫 번째 서버나 가상 컴퓨터를 등록 하면 저장소 유형이 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="9d7ba-131">그 이후에는 저장소 유형을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9d7ba-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="9d7ba-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d7ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="9d7ba-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d7ba-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="9d7ba-134">새로운 AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d7ba-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="9d7ba-135">제거-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d7ba-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


