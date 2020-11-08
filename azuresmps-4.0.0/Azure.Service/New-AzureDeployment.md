---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045929"
---
# <span data-ttu-id="b8693-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b8693-101">New-AzureDeployment</span></span>

## <span data-ttu-id="b8693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8693-102">SYNOPSIS</span></span>
<span data-ttu-id="b8693-103">서비스에서 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="b8693-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8693-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8693-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8693-105">DESCRIPTION</span></span>
<span data-ttu-id="b8693-106">**새-AzureDeployment** cmdlet은 웹 역할 및 작업자 역할로 구성 된 서비스에서 Azure 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="b8693-107">이 cmdlet은 패키지 파일 (cspkg) 및 서비스 구성 파일 (.cscfg)을 기반으로 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="b8693-108">배포 환경 내에서 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="b8693-109">**새 add-azurevm** cmdlet을 사용 하 여 Azure 가상 컴퓨터를 기반으로 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="b8693-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8693-110">EXAMPLES</span></span>

### <span data-ttu-id="b8693-111">예제 1: 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="b8693-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="b8693-112">이 명령은 ContosoPackage kg 이라는 패키지와 ContosoConfiguration 이라는 구성에 따라 프로덕션 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="b8693-113">명령은 배포에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="b8693-114">이름은 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-114">It does not specify a name.</span></span>
<span data-ttu-id="b8693-115">이 cmdlet은 이름으로 GUID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="b8693-116">예제 2: 확장 구성을 기반으로 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="b8693-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="b8693-117">이 명령은 패키지와 구성을 기반으로 프로덕션 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="b8693-118">명령에서 ContosoExtensionConfig 라는 확장 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="b8693-119">이 cmdlet은 이름 및 레이블로 Guid를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="b8693-120">변수</span><span class="sxs-lookup"><span data-stu-id="b8693-120">PARAMETERS</span></span>

### <span data-ttu-id="b8693-121">-구성</span><span class="sxs-lookup"><span data-stu-id="b8693-121">-Configuration</span></span>
<span data-ttu-id="b8693-122">서비스 구성 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8693-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="b8693-123">-DoNotStart</span></span>
<span data-ttu-id="b8693-124">이 cmdlet이 배포를 시작 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="b8693-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8693-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="b8693-126">확장 구성 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8693-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8693-127">-InformationAction</span></span>
<span data-ttu-id="b8693-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8693-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8693-130">하기로</span><span class="sxs-lookup"><span data-stu-id="b8693-130">Continue</span></span>
- <span data-ttu-id="b8693-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="b8693-131">Ignore</span></span>
- <span data-ttu-id="b8693-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="b8693-132">Inquire</span></span>
- <span data-ttu-id="b8693-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8693-133">SilentlyContinue</span></span>
- <span data-ttu-id="b8693-134">중지가</span><span class="sxs-lookup"><span data-stu-id="b8693-134">Stop</span></span>
- <span data-ttu-id="b8693-135">대기</span><span class="sxs-lookup"><span data-stu-id="b8693-135">Suspend</span></span>

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

### <span data-ttu-id="b8693-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8693-136">-InformationVariable</span></span>
<span data-ttu-id="b8693-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8693-138">-레이블</span><span class="sxs-lookup"><span data-stu-id="b8693-138">-Label</span></span>
<span data-ttu-id="b8693-139">배포의 레이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="b8693-140">레이블을 지정 하지 않으면이 cmdlet은 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8693-141">-이름</span><span class="sxs-lookup"><span data-stu-id="b8693-141">-Name</span></span>
<span data-ttu-id="b8693-142">배포 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-142">Specifies a deployment name.</span></span>
<span data-ttu-id="b8693-143">이름을 지정 하지 않으면이 cmdlet은 GUID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8693-144">-패키지</span><span class="sxs-lookup"><span data-stu-id="b8693-144">-Package</span></span>
<span data-ttu-id="b8693-145">동일한 구독 또는 프로젝트 내의 저장소에서 cspkg 파일의 경로 또는 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8693-146">-프로필</span><span class="sxs-lookup"><span data-stu-id="b8693-146">-Profile</span></span>
<span data-ttu-id="b8693-147">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8693-148">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8693-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8693-149">-ServiceName</span></span>
<span data-ttu-id="b8693-150">배포에 대 한 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-150">Specifies the name of the Azure service for the deployment.</span></span>

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

### <span data-ttu-id="b8693-151">-슬롯</span><span class="sxs-lookup"><span data-stu-id="b8693-151">-Slot</span></span>
<span data-ttu-id="b8693-152">이 cmdlet이 배포를 만드는 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="b8693-153">유효한 값은 스테이징 및 프로덕션입니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="b8693-154">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8693-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="b8693-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="b8693-156">경고 메시지가 오류 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="b8693-157">이 매개 변수를 지정 하면 경고 메시지로 인해 배포에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="b8693-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8693-158">CommonParameters</span></span>
<span data-ttu-id="b8693-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8693-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8693-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8693-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8693-161">입력</span><span class="sxs-lookup"><span data-stu-id="b8693-161">INPUTS</span></span>

## <span data-ttu-id="b8693-162">출력</span><span class="sxs-lookup"><span data-stu-id="b8693-162">OUTPUTS</span></span>

## <span data-ttu-id="b8693-163">상속자</span><span class="sxs-lookup"><span data-stu-id="b8693-163">NOTES</span></span>

## <span data-ttu-id="b8693-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8693-164">RELATED LINKS</span></span>

[<span data-ttu-id="b8693-165">다운로드-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b8693-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="b8693-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="b8693-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="b8693-167">이동-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b8693-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="b8693-168">뉴욕</span><span class="sxs-lookup"><span data-stu-id="b8693-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="b8693-169">-AzureDeployment 제거</span><span class="sxs-lookup"><span data-stu-id="b8693-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="b8693-170">Set AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b8693-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


