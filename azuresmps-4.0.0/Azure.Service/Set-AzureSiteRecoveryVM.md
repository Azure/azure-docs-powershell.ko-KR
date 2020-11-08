---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045754"
---
# <span data-ttu-id="eadb4-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="eadb4-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="eadb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eadb4-102">SYNOPSIS</span></span>
<span data-ttu-id="eadb4-103">사이트 복구 보호 엔터티의 복구 쪽 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="eadb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eadb4-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eadb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eadb4-105">DESCRIPTION</span></span>
<span data-ttu-id="eadb4-106">**AzureSiteRecoveryVM** cmdlet은 복구 가상 컴퓨터 크기 및 복구 가상 컴퓨터 네트워크와 같은 Azure Site recovery 보호 엔터티의 복구 쪽 보호 옵션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="eadb4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eadb4-107">EXAMPLES</span></span>

### <span data-ttu-id="eadb4-108">예제 1: 보호 된 가상 컴퓨터에서 업데이트 허용</span><span class="sxs-lookup"><span data-stu-id="eadb4-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="eadb4-109">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 protected 컨테이너를 얻은 다음 $ProtectionContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="eadb4-110">두 번째 명령은 **AzureSiteRecoveryVM** cmdlet을 사용 하 여 $ProtectionContainer의 가상 컴퓨터를 가져온 다음 $VitrualMachines 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="eadb4-111">마지막 명령은 NewVirtualMachine05 이라는 $VitrualMachines 배열의 첫 번째 가상 컴퓨터에 대 한 업데이트를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="eadb4-112">변수</span><span class="sxs-lookup"><span data-stu-id="eadb4-112">PARAMETERS</span></span>

### <span data-ttu-id="eadb4-113">-이름</span><span class="sxs-lookup"><span data-stu-id="eadb4-113">-Name</span></span>
<span data-ttu-id="eadb4-114">대상 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-114">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadb4-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="eadb4-115">-PrimaryNic</span></span>
<span data-ttu-id="eadb4-116">주 네트워크 어댑터 카드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-116">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadb4-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="eadb4-117">-Profile</span></span>
<span data-ttu-id="eadb4-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eadb4-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadb4-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="eadb4-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="eadb4-121">복구 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadb4-122">-크기</span><span class="sxs-lookup"><span data-stu-id="eadb4-122">-Size</span></span>
<span data-ttu-id="eadb4-123">대상 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-123">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadb4-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eadb4-124">-VirtualMachine</span></span>
<span data-ttu-id="eadb4-125">사이트 복구 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eadb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadb4-126">CommonParameters</span></span>
<span data-ttu-id="eadb4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadb4-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eadb4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadb4-129">입력</span><span class="sxs-lookup"><span data-stu-id="eadb4-129">INPUTS</span></span>

## <span data-ttu-id="eadb4-130">출력</span><span class="sxs-lookup"><span data-stu-id="eadb4-130">OUTPUTS</span></span>

## <span data-ttu-id="eadb4-131">상속자</span><span class="sxs-lookup"><span data-stu-id="eadb4-131">NOTES</span></span>

## <span data-ttu-id="eadb4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eadb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="eadb4-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eadb4-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="eadb4-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="eadb4-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


