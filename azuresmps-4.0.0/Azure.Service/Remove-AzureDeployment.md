---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046165"
---
# <span data-ttu-id="d91af-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d91af-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="d91af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91af-102">SYNOPSIS</span></span>
<span data-ttu-id="d91af-103">클라우드 서비스의 배포를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="d91af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d91af-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d91af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d91af-105">DESCRIPTION</span></span>
<span data-ttu-id="d91af-106">**-Azuredeployment** Cmdlet은 Azure 클라우드 서비스의 배포를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="d91af-107">배포를 삭제 하려면 먼저 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="d91af-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d91af-108">EXAMPLES</span></span>

### <span data-ttu-id="d91af-109">예제 1: 배포 제거</span><span class="sxs-lookup"><span data-stu-id="d91af-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="d91af-110">이 명령은 ContosoService 이라는 Azure 서비스의 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="d91af-111">이 명령은 슬롯을 지정 하지 않으므로 프로덕션 환경에서 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="d91af-112">예제 2: 배포 및 가상 하드 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="d91af-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="d91af-113">이 명령은 프로덕션 환경에서 ContosoService 이라는 서비스의 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="d91af-114">또한이 명령은 기본 가상 하드 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="d91af-115">변수</span><span class="sxs-lookup"><span data-stu-id="d91af-115">PARAMETERS</span></span>

### <span data-ttu-id="d91af-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="d91af-116">-DeleteVHD</span></span>
<span data-ttu-id="d91af-117">이 cmdlet이 blob 저장소에서 배포 및 Vhd (가상 하드 디스크)를 제거 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d91af-118">-Force</span></span>
<span data-ttu-id="d91af-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91af-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d91af-120">-InformationAction</span></span>
<span data-ttu-id="d91af-121">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d91af-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d91af-123">하기로</span><span class="sxs-lookup"><span data-stu-id="d91af-123">Continue</span></span>
- <span data-ttu-id="d91af-124">숨기기</span><span class="sxs-lookup"><span data-stu-id="d91af-124">Ignore</span></span>
- <span data-ttu-id="d91af-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="d91af-125">Inquire</span></span>
- <span data-ttu-id="d91af-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d91af-126">SilentlyContinue</span></span>
- <span data-ttu-id="d91af-127">중지가</span><span class="sxs-lookup"><span data-stu-id="d91af-127">Stop</span></span>
- <span data-ttu-id="d91af-128">대기</span><span class="sxs-lookup"><span data-stu-id="d91af-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91af-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d91af-129">-InformationVariable</span></span>
<span data-ttu-id="d91af-130">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91af-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="d91af-131">-Profile</span></span>
<span data-ttu-id="d91af-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d91af-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d91af-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d91af-134">-ServiceName</span></span>
<span data-ttu-id="d91af-135">이 cmdlet이 배포를 삭제 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91af-136">-슬롯</span><span class="sxs-lookup"><span data-stu-id="d91af-136">-Slot</span></span>
<span data-ttu-id="d91af-137">이 cmdlet이 배포를 삭제 하는 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="d91af-138">유효한 값은 스테이징 및 프로덕션입니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="d91af-139">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91af-140">CommonParameters</span></span>
<span data-ttu-id="d91af-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d91af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91af-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d91af-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91af-143">입력</span><span class="sxs-lookup"><span data-stu-id="d91af-143">INPUTS</span></span>

## <span data-ttu-id="d91af-144">출력</span><span class="sxs-lookup"><span data-stu-id="d91af-144">OUTPUTS</span></span>

### <span data-ttu-id="d91af-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="d91af-145">ManagementOperationContext</span></span>

## <span data-ttu-id="d91af-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d91af-146">NOTES</span></span>

## <span data-ttu-id="d91af-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d91af-147">RELATED LINKS</span></span>

[<span data-ttu-id="d91af-148">다운로드-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d91af-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="d91af-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="d91af-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="d91af-150">이동-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d91af-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="d91af-151">새 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d91af-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="d91af-152">Set AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d91af-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


